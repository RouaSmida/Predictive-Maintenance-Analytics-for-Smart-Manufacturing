# Data Dictionary – Predictive Maintenance BI

## Fact_MachineEvents

- **EventID**: Surrogate key for each machine reading (integer).
- **DateID**: Foreign key to Dim_Date (YYYYMMDD integer).
- **MachineID**: Foreign key to Dim_Machine.
- **ProductTypeID**: Foreign key to Dim_ProductType.
- **AirTempC**: Air temperature around the machine in degrees Celsius.
- **ProcessTempC**: Process temperature during the operation in degrees Celsius.
- **RotationalSpeed**: Rotational speed of the tool in rpm.
- **Torque**: Torque applied during the operation in Nm.
- **ToolWear**: Cumulative tool usage in minutes.
- **MachineFailure**: 1 if any failure occurred during the cycle, 0 otherwise.
- **TWF**: Tool wear failure indicator (1/0).
- **HDF**: Heat dissipation failure indicator (1/0).
- **PWF**: Power failure indicator (1/0).
- **OSF**: Overstrain failure indicator (1/0).
- **RNF**: Random failure indicator (1/0).

## Dim_ProductType

- **ProductTypeID**: Surrogate key for product type.
- **ProductType**: Product variant label (L, M, H).

## Dim_Date

- **DateID**: Surrogate key for the calendar date (YYYYMMDD).
- **Date**: Calendar date.
- **Day**: Day of month (1–31).
- **Month**: Month number (1–12).
- **Quarter**: Quarter of the year (1–4).
- **Year**: Year (e.g., 2025).
- **Shift**: Simple shift label (e.g., “Day”).

## Dim_Machine

- **MachineID**: Surrogate key for the machine.
- **MachineName**: Human‑readable machine name (Machine A, B, C).
- **Line**: Production line name.
- **Location**: Plant or site where the machine is installed.
