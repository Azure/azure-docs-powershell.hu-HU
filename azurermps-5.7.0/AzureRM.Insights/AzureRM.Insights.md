---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490584"
---
# AzureRM. a betekintést ismertető modul
## Leírás
Ez a témakör az Azure Insight-parancsmagokkal kapcsolatos súgótémaköröket jeleníti meg.

## AzureRM. a betekintést szolgáló parancsmagok
### [Add-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
Egy automéretarányos beállítást hoz létre.

### [Add-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
Naplózási riasztási szabály hozzáadása vagy cseréje

### [Add-AzureRmLogProfile](Add-AzureRmLogProfile.md)
Új műveletnapló-profilt hoz létre. Ezzel a profillal a tevékenység naplóját Azure-tárterületre archiválhatja, vagy ugyanazon előfizetésben továbbíthatja egy Azure Event hub-ra. 

- **Storage Account** -only standard Storage Account (prémium tárterület-fiók nem támogatott) támogatott. Lehet, hogy a kar vagy a klasszikus típus közül kell lennie. Ha egy tárolási fiókba van bejelentkezve, a műveletnapló tárolási költségét a normál szokásos tárolási áron számlázzák. Egy előfizetésben csak egy log-profil lehet, egy előfizetésben csak egy tárterület-fiók használható a műveletnapló exportálásához. 

- **Esemény-hub** : egy előfizetésben csak egy naplózási profil lehet, az előfizetéssel csak egy esemény-előfizetéssel exportálható a tevékenység naplója. Ha a műveletnapló egy esemény központjának van továbbítva, a normál esemény hub árazása érvényes lesz. 

A tevékenység naplóban az események egy régióra vonatkozhat vagy "globálisak" lehetnek. Globális lényegében azt jelenti, hogy ezek az események a régió agnosztikusok és függetlenek a régiótól, az események többsége ebbe a kategóriába esik. Ha a műveletnapló profilja a portálról van beállítva, implicit módon felveszi a "globális" kifejezést a felhasználói felületen kijelölt többi régióval együtt. A parancsmag használatakor a "globális" helyet külön meg kell említeni a többi régióban kívül. 

**Megjegyzés** : **a helyek "globális" beállításának hiánya következtében a tevékenység naplójának többsége nem fog exportálni.** 

### [Add-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
Metrika-alapú figyelmeztetési szabály hozzáadása vagy frissítése

### [Add-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Webteszt figyelmeztetési szabály hozzáadása vagy frissítése

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
Letiltja a műveletnapló riasztását, és beállítja annak címkéit.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
Engedélyezi a műveletnapló riasztását, és beállítja annak címkéit.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
A műveleti csoport (ok) beolvasása

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
Egy vagy több tevékenység naplója riasztási erőforrást kap.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
Megkapja az értesítések előzményeit.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
Figyelmeztetési szabályokat kap.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
Megkapja az autoscale előzményeit.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
Az automéretarány beállításai.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
A naplózott kategóriák és időgabonák beolvasása

### [Get-AzureRmLog](Get-AzureRmLog.md)
Naplózza az eseményeket.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
Log-profilt kap.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
Egy erőforrás metrikus értékeit kapja meg.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
Metrikus definíciókat kap.

### [Get-AzureRmUsage](Get-AzureRmUsage.md)
Az erőforrás használati metrikáját kapja meg.

### [Új – AzureRmActionGroup](New-AzureRmActionGroup.md)
Egy ActionGroup-viszonyítási objektumot hoz létre a memóriában.

### [Új – AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
Új akciócsoport-vevőkészülék létrehozása.

### [Új – AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
Új tevékenység-naplózási riasztási feltétel objektum létrehozása a memóriában.

### [Új – AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
E-mail-művelet létrehozása egy figyelmeztetési szabályhoz.

### [Új – AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
Figyelmeztetési szabályt hoz létre.

### [Új – AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
E-mail-értesítést hoz létre.

### [Új – AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
Automéretarányos profilt hoz létre.

### [Új – AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
Egy automéretarányos szabályt hoz létre.

### [Új – AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
Automatikusan létrehoz egy automéretarányos webkampót.

### [Remove-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
Egy művelet csoportjának eltávolítása.

### [Remove-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
Tevékenység-naplózási riasztás eltávolítása.

### [Remove-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
Figyelmeztetési szabály eltávolítása

### [Remove-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
Az automéretarány beállítás eltávolítása

### [Remove-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
A napló-profil eltávolítása.

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
Új vagy frissített meglévő műveleti csoport létrehozása

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
Új vagy meglévő tevékenység-naplózási riasztást hoz létre.

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
Az erőforrás naplók és metrikák beállításainak beállítása.

