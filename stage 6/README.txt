IEEE 30-BUS AIP TOOL — PSS/E TEST FILES
=========================================
Generated for AIP Technical Evaluation Platform — Stage 6

FILE LIST
---------
RAW NETWORK FILES (upload to File Input > PSS/E RAW):
  IEEE30_AO1.raw   — Full IEEE 30-Bus base case (v33 format)
  IEEE30_S1.raw   — S1 with 30-Bus base case with Bus28+29 (v33 format)
  IEEE30_S2.raw   — S2 with 30-Bus base case with Bus27+29 + Gen Bus32 200MW (v33 format)
  IEEE30_S3.raw    — S3 with Bus 31/32/33 added

LOAD FLOW CSV (upload to File Input > Load Flow):
  AO1_loadflow.csv — Base case bus voltages and flows
  S1_loadflow.csv  — S1: Bus31 via Bus28+29 (no gen)
  S2_loadflow.csv  — S2: Bus31 via Bus27+29 + Gen Bus32 200MW
  S3_loadflow.csv  — S3: Bus31 via Bus28+30 + Gen Bus32 400MW + Bus33 300MW

CONTINGENCY ACC (upload to File Input > Contingency ACCC):
  AO1_contingency.acc
  S1_contingency.acc
  S2_contingency.acc
  S3_contingency.acc

SHORT CIRCUIT DAT (upload to File Input > Short Circuit):
  AO1_shortcircuit.dat
  S3_shortcircuit.dat

TRANSIENT OUT (upload to File Input > Transient Stability):
  AO1_transient.out
  S3_transient.out

EXPECTED RATINGS
----------------
  AO1 = Very Good  (0 compliance fails, 2 strategic gaps)
  S1  = Bad        (2 compliance fails: post-fault V, post-comp V)
  S2  = Good       (0 compliance fails, 13 strategic gaps)
  S3  = Excellent  (0 compliance fails, 0 strategic gaps)

CSV FORMAT (for paste import)
-----------------------------
Load Flow:    bus,name,type,v_pu,angle_deg,pgen_mw,qgen_mvar,pload_mw,qload_mvar,ploss_mw
Contingency:  cont_id,label,type,element,post_flow_mva,post_loading_pct,rating_mva,viol_bus,pre_v_pu,post_v_pu,delta_v,status
Short Circuit:bus,name,kv_base,i_fault_3ph_ka,i_fault_pu,xr_ratio,breaker_duty_pct,severity
Transient:    time_s,bus1_v_pu,bus6_v_pu,gen1_angle_deg,gen2_angle_deg,gen1_speed_pu,freq_hz
