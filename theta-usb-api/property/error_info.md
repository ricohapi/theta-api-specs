# 0xD006 ErrorInfo

### Device Prop Code

0xD006

### Overview

Acquires error information.   
(Vendor Extension Property)

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | All | All | All |

### Support Value

#### RICOH THETA X

<table>
    <thead>
      <tr>
        <th width="15%">Value</th>
        <th width="15%">Error code</th>
        <th width="10%">Can/not shoot</th>
        <th width="30%">Desription</th>
        <th width="30%">Recommended action</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>0x00000001</td>
        <td>Insufficient memory</td>
        <td></td>
        <td>Issued when the shutter release button is pressed while the number of remaining available shots is "0".</td>
        <td>Delete files</td>
      </tr>
      <tr>
        <td>0x00000004</td>
        <td>Excessive file number</td>
        <td></td>
        <td>Issued when the maximum file number is exceeded.<br>Restored by resetting the file number.</td>
        <td>Delete 999 folder or delete 9999 file</td>
      </tr>
      <tr>
        <td>0x00000008</td>
        <td>Clock unset</td>
        <td>✓</td>
        <td>Issued when the internal clock of the camera is not set.</td>
        <td>Set Date/Time via API, UI, or NTP</td>
      </tr>
      <tr>
        <td>0x00000010 *2</td>
        <td>Electronic compass error</td>
        <td>✓</td>
        <td>Issued when there is an error with the electronic compass.</td>
        <td>Move the camera with ∞ pattern</td>
      </tr>
      <tr>
        <td>0x00000020</td>
        <td>Not supported media type</td>
        <td>✓</td>
        <td>Unsupported media (SDHC, etc.)</td>
        <td>Use microSDXC card</td>
      </tr>
      <tr>
        <td>0x00000040</td>
        <td>Not supported file system</td>
        <td>✓</td>
        <td>Unsupported format (FAT32, etc.)</td>
        <td>Format the microSD card</td>
      </tr>
      <tr>
        <td>0x00000100</td>
        <td>Media not ready</td>
        <td>✓</td>
        <td>Error warning while mounting</td>
        <td>Wait for the microSD card is mounted</td>
      </tr>
      <tr>
        <td>0x00000200</td>
        <td>Not enough battery</td>
        <td>✓</td>
        <td>Battery level warning (firmware update)</td>
        <td>Charge battery</td>
      </tr>
      <tr>
        <td>0x00000400</td>
        <td>Invalid file</td>
        <td>✓</td>
        <td>Firmware file mismatch warning</td>
        <td>Retry firmware update</td>
      </tr>
      <tr>
        <td>0x00000800</td>
        <td>Plugin boot error </td>
        <td>✓</td>
        <td>Plugin start warning (IoT technical standards compliance)</td> <td>Disconnect from internet</td>
      </tr>
      <tr>
        <td>0x00001000</td>
        <td>In progress error</td>
        <td></td>
        <td>When performing continuous shooting by operating the camera while executing &lt;Delete object&gt;, &lt;Transfer firmware file&gt;, &lt;Install plugin&gt; or &lt;Uninstall plugin&gt; with the WebAPI or MTP.</td>
        <td>Wait for the processing finished</td>
      </tr>
      <tr>
        <td>0x00001000</td>
        <td>Cannot recording</td>
        <td></td>
        <td>Battery inserted + WLAN ON + Video mode + 4K 60fps / 5.7K 10fps / 5.7K 15fps / 5.7K 30fps / 8K 10fps</td>
        <td>Turn off WLAN</td>
      </tr>
      <tr>
        <td>0x00002000</td>
        <td>Cannot record for low battery</td>
        <td></td>
        <td>Battery inserted AND Specified battery level or lower + WLAN ON + Video mode + 4K 30fps</td>
        <td>Charge the battery</td>
      </tr>
      <tr>
        <td>0x00400000</td>
        <td>Shooting hardware failure detection</td>
        <td></td>
        <td>Issued when a failure has been detected with hardware used for shooting.</td>
        <td>Reboot the camera may help</td>
      </tr>
      <tr>
        <td>0x00800000</td>
        <td>Software error</td>
        <td></td>
        <td>Software error.</td>
        <td>Reboot the camera may help</td>
      </tr>
      <tr>
        <td>0x08000000</td>
        <td>Internal memory access error</td>
        <td></td>
        <td>Issued when the internal memory of the camera cannot be accessed.</td>
        <td>Reboot the camera may help</td>
      </tr>
      <tr>
        <td>0x20000000</td>
        <td>Miscellaneous error</td>
        <td></td>
        <td>An error other than above.</td>
        <td>Reboot the camera may help</td>
      </tr>
      <tr>
        <td>0x40000000</td>
        <td>Charging error</td>
        <td></td>
        <td>Issued when the a USB charging error has been detected. The camera is powered off when this error occurs.</td>
        <td>Check USB cable or charger</td>
      </tr>
      <tr>
        <td>0x00100000 *1</td>
        <td>(Board) temperature warning</td>
        <td>✓</td>
        <td>Issued when the internal temperature of the camera is close to the upper limit temperature.</td>
        <td>Cool the camera</td>
      </tr>
      <tr>
        <td>0x80000000</td>
        <td>(Board) temperature error</td>
        <td></td>
        <td>Issued when the internal temperature of the camera is higher than the upper limit temperature. The camera is powered off when this error occurs.</td>
        <td>Cool the camera</td>
      </tr>
      <tr>
        <td>0x00200000</td>
        <td>Battery temperature error</td>
        <td></td>
        <td>Issued when the battery temperature of the camera is higher than the upper limit temperature. The camera is powered off when this error occurs.</td>
        <td>Cool the camera</td>
      </tr>
    </tbody>
  </table>  

\*1 RICOH THETA X firmware v1.40.0 or later
\*2 RICOH THETA X firmware v2.40.0 or later

#### RICOH THETA Z1 or prior

<table>
    <thead>
      <tr>
        <th width="15%">Value</th>
        <th width="15%">Error code</th>
        <th width="10%">Can/not shoot</th>
        <th width="30%">Desription</th>
        <th width="30%">Recommended action</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>0x00000001</td>
        <td>Insufficient memory</td>
        <td></td>
        <td>Issued when the shutter release button is pressed while the number of remaining available shots is "0".</td>
        <td>Delete files</td>
      </tr>
      <tr>
        <td>0x00000004</td>
        <td>Excessive file number</td>
        <td></td>
        <td>Issued when the maximum file number is exceeded.<br>Restored by resetting the file number.</td>
        <td>Delete 999 folder or delete 9999 file</td>
      </tr>
      <tr>
        <td>0x00000008</td>
        <td>Clock unset</td>
        <td>✓</td>
        <td>Issued when the internal clock of the camera is not set.</td>
        <td>Set Date/Time via API, UI, or NTP</td>
      </tr>
      <tr>
        <td>0x00000010</td>
        <td>Electronic compass error</td>
        <td>✓</td>
        <td>Issued when there is an error with the electronic compass.</td>
        <td>Move the camera with ∞ pattern</td>
      </tr>
      <tr>
        <td>0x00000800 *1</td>
        <td>Plugin boot error </td>
        <td>✓</td>
        <td>Plugin start warning (IoT technical standards compliance)</td> <td>Disconnect from internet</td>
      </tr>
      <tr>
        <td>0x00100000 *2</td>
        <td>(Board) temperature warning</td>
        <td>✓</td>
        <td>Issued when the internal temperature of the camera is close to the upper limit temperature.</td>
        <td>Cool the camera</td>
      </tr>
      <tr>
        <td>0x00400000</td>
        <td>Shooting hardware failure detection</td>
        <td></td>
        <td>Issued when a failure has been detected with hardware used for shooting.</td>
        <td>Reboot the camera may help</td>
      </tr>
      <tr>
        <td>0x08000000</td>
        <td>Internal memory access error</td>
        <td></td>
        <td>Issued when the internal memory of the camera cannot be accessed.</td>
        <td>Reboot the camera may help</td>
      </tr>
      <tr>
        <td>0x20000000</td>
        <td>Miscellaneous error</td>
        <td></td>
        <td>An error other than above.</td>
        <td>Reboot the camera may help</td>
      </tr>
      <tr>
        <td>0x40000000</td>
        <td>Charging error</td>
        <td></td>
        <td>Issued when the a USB charging error has been detected. The camera is powered off when this error occurs.</td>
        <td>Check USB cable or charger</td>
      </tr>
      <tr>
        <td>0x80000000</td>
        <td>(Board) temperature error</td>
        <td></td>
        <td>Issued when the internal temperature of the camera is higher than the upper limit temperature. The camera is powered off when this error occurs.</td>
        <td>Cool the camera</td>
      </tr>
      <tr>
        <td>0x00200000 *1</td>
        <td>Battery temperature error</td>
        <td></td>
        <td>Issued when the battery temperature of the camera is higher than the upper limit temperature. The camera is powered off when this error occurs.</td>
        <td>Cool the camera</td>
      </tr>
    </tbody>
  </table>  

\*1 RICOH THETA Z1 or later  
\*2 RICOH THETA Z1 v2.20.3 or later  
