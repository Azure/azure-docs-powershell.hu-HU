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
# <span data-ttu-id="89b82-101">AzureRM. a betekintést ismertető modul</span><span class="sxs-lookup"><span data-stu-id="89b82-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="89b82-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="89b82-102">Description</span></span>
<span data-ttu-id="89b82-103">Ez a témakör az Azure Insight-parancsmagokkal kapcsolatos súgótémaköröket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="89b82-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="89b82-104">AzureRM. a betekintést szolgáló parancsmagok</span><span class="sxs-lookup"><span data-stu-id="89b82-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="89b82-105">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="89b82-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="89b82-106">Egy automéretarányos beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89b82-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="89b82-107">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="89b82-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="89b82-108">Naplózási riasztási szabály hozzáadása vagy cseréje</span><span class="sxs-lookup"><span data-stu-id="89b82-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="89b82-109">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="89b82-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="89b82-110">Új műveletnapló-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89b82-110">Creates a new activity log profile.</span></span> <span data-ttu-id="89b82-111">Ezzel a profillal a tevékenység naplóját Azure-tárterületre archiválhatja, vagy ugyanazon előfizetésben továbbíthatja egy Azure Event hub-ra.</span><span class="sxs-lookup"><span data-stu-id="89b82-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="89b82-112">**Storage Account** -only standard Storage Account (prémium tárterület-fiók nem támogatott) támogatott.</span><span class="sxs-lookup"><span data-stu-id="89b82-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="89b82-113">Lehet, hogy a kar vagy a klasszikus típus közül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="89b82-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="89b82-114">Ha egy tárolási fiókba van bejelentkezve, a műveletnapló tárolási költségét a normál szokásos tárolási áron számlázzák.</span><span class="sxs-lookup"><span data-stu-id="89b82-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="89b82-115">Egy előfizetésben csak egy log-profil lehet, egy előfizetésben csak egy tárterület-fiók használható a műveletnapló exportálásához.</span><span class="sxs-lookup"><span data-stu-id="89b82-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="89b82-116">**Esemény-hub** : egy előfizetésben csak egy naplózási profil lehet, az előfizetéssel csak egy esemény-előfizetéssel exportálható a tevékenység naplója.</span><span class="sxs-lookup"><span data-stu-id="89b82-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="89b82-117">Ha a műveletnapló egy esemény központjának van továbbítva, a normál esemény hub árazása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="89b82-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="89b82-118">A tevékenység naplóban az események egy régióra vonatkozhat vagy "globálisak" lehetnek.</span><span class="sxs-lookup"><span data-stu-id="89b82-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="89b82-119">Globális lényegében azt jelenti, hogy ezek az események a régió agnosztikusok és függetlenek a régiótól, az események többsége ebbe a kategóriába esik.</span><span class="sxs-lookup"><span data-stu-id="89b82-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="89b82-120">Ha a műveletnapló profilja a portálról van beállítva, implicit módon felveszi a "globális" kifejezést a felhasználói felületen kijelölt többi régióval együtt.</span><span class="sxs-lookup"><span data-stu-id="89b82-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="89b82-121">A parancsmag használatakor a "globális" helyet külön meg kell említeni a többi régióban kívül.</span><span class="sxs-lookup"><span data-stu-id="89b82-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="89b82-122">**Megjegyzés** : **a helyek "globális" beállításának hiánya következtében a tevékenység naplójának többsége nem fog exportálni.**</span><span class="sxs-lookup"><span data-stu-id="89b82-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="89b82-123">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="89b82-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="89b82-124">Metrika-alapú figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="89b82-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="89b82-125">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="89b82-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="89b82-126">Webteszt figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="89b82-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="89b82-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="89b82-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="89b82-128">Letiltja a műveletnapló riasztását, és beállítja annak címkéit.</span><span class="sxs-lookup"><span data-stu-id="89b82-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="89b82-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="89b82-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="89b82-130">Engedélyezi a műveletnapló riasztását, és beállítja annak címkéit.</span><span class="sxs-lookup"><span data-stu-id="89b82-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="89b82-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="89b82-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="89b82-132">A műveleti csoport (ok) beolvasása</span><span class="sxs-lookup"><span data-stu-id="89b82-132">Gets action group(s).</span></span>

### [<span data-ttu-id="89b82-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="89b82-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="89b82-134">Egy vagy több tevékenység naplója riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="89b82-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="89b82-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="89b82-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="89b82-136">Megkapja az értesítések előzményeit.</span><span class="sxs-lookup"><span data-stu-id="89b82-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="89b82-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="89b82-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="89b82-138">Figyelmeztetési szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="89b82-138">Gets alert rules.</span></span>

### [<span data-ttu-id="89b82-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="89b82-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="89b82-140">Megkapja az autoscale előzményeit.</span><span class="sxs-lookup"><span data-stu-id="89b82-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="89b82-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="89b82-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="89b82-142">Az automéretarány beállításai.</span><span class="sxs-lookup"><span data-stu-id="89b82-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="89b82-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="89b82-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="89b82-144">A naplózott kategóriák és időgabonák beolvasása</span><span class="sxs-lookup"><span data-stu-id="89b82-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="89b82-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="89b82-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="89b82-146">Naplózza az eseményeket.</span><span class="sxs-lookup"><span data-stu-id="89b82-146">Gets a log of events.</span></span>

### [<span data-ttu-id="89b82-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="89b82-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="89b82-148">Log-profilt kap.</span><span class="sxs-lookup"><span data-stu-id="89b82-148">Gets a log profile.</span></span>

### [<span data-ttu-id="89b82-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="89b82-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="89b82-150">Egy erőforrás metrikus értékeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="89b82-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="89b82-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="89b82-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="89b82-152">Metrikus definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="89b82-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="89b82-153">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="89b82-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="89b82-154">Az erőforrás használati metrikáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="89b82-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="89b82-155">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="89b82-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="89b82-156">Egy ActionGroup-viszonyítási objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="89b82-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="89b82-157">Új – AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="89b82-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="89b82-158">Új akciócsoport-vevőkészülék létrehozása.</span><span class="sxs-lookup"><span data-stu-id="89b82-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="89b82-159">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="89b82-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="89b82-160">Új tevékenység-naplózási riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="89b82-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="89b82-161">Új – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="89b82-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="89b82-162">E-mail-művelet létrehozása egy figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="89b82-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="89b82-163">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="89b82-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="89b82-164">Figyelmeztetési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89b82-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="89b82-165">Új – AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="89b82-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="89b82-166">E-mail-értesítést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89b82-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="89b82-167">Új – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="89b82-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="89b82-168">Automéretarányos profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89b82-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="89b82-169">Új – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="89b82-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="89b82-170">Egy automéretarányos szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89b82-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="89b82-171">Új – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="89b82-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="89b82-172">Automatikusan létrehoz egy automéretarányos webkampót.</span><span class="sxs-lookup"><span data-stu-id="89b82-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="89b82-173">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="89b82-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="89b82-174">Egy művelet csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="89b82-174">Removes an action group.</span></span>

### [<span data-ttu-id="89b82-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="89b82-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="89b82-176">Tevékenység-naplózási riasztás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="89b82-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="89b82-177">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="89b82-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="89b82-178">Figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="89b82-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="89b82-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="89b82-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="89b82-180">Az automéretarány beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="89b82-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="89b82-181">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="89b82-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="89b82-182">A napló-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="89b82-182">Removes a log profile.</span></span>

### [<span data-ttu-id="89b82-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="89b82-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="89b82-184">Új vagy frissített meglévő műveleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="89b82-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="89b82-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="89b82-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="89b82-186">Új vagy meglévő tevékenység-naplózási riasztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89b82-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="89b82-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="89b82-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="89b82-188">Az erőforrás naplók és metrikák beállításainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="89b82-188">Sets the logs and metrics settings for the resource.</span></span>

