# RotationalParameters
Rotational parameters for sources


Columns marked with an exclamation mark (❗️) may not be empty.
| Column Name | Description | Datatype | Length | Units  | UCD |
| --- | --- | --- | --- | --- | --- |
| ❗️ <ins>source</ins> | Main identifier for an object; links to Sources table | string | 50 |  | meta.id;meta.main  |
| period_hr | Rotational period in hours | double |  | hr | time.period  |
| period_error | Uncertainty of the rotational period | double |  | hr | stat.error;time.period  |
| v_sin_i_kms | Projected rotational velocity in km/s | double |  | km/s | phys.veloc.rotat  |
| v_sin_i_error | Uncertainty of the projected rotational velocity | double |  | km/s | stat.error;phys.veloc.rotat  |
| inclination | Inclination of the rotation axis in degrees | double |  | deg | src.orbital.inclination  |
| inclination_error | Uncertainty of the inclination | double |  | deg | stat.error;src.orbital.inclination  |
| adopted | Flag to indicate if this is the adopted entry | boolean |  |  | meta.code  |
| comments | Free-form comments for this entry | string | 100 |  | meta.note  |
| ❗️ <ins>reference</ins> | Publication reference; links to Publications table | string | 30 |  | meta.ref  |

## Indexes
| Name | Columns | Description |
| --- | --- | --- |
| PK_RotationalParameters | ['#RotationalParameters.source', '#RotationalParameters.reference'] | Primary key for RotationalParameters table |

## Foreign Keys
| Description | Columns | Referenced Columns |
| --- | --- | --- |
| Link RotationalParameters source to Sources table | ['#RotationalParameters.source'] | ['#Sources.source'] |
| Link RotationalParameters reference to Publications table | ['#RotationalParameters.reference'] | ['#Publications.reference'] |
