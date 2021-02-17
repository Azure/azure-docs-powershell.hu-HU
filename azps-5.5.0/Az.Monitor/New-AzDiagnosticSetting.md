---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147379"
---
# <span data-ttu-id="483e7-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="483e7-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="483e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483e7-102">SYNOPSIS</span></span>
<span data-ttu-id="483e7-103">PSServiceDiagnosticSettings objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="483e7-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="483e7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="483e7-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="483e7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="483e7-105">DESCRIPTION</span></span>
<span data-ttu-id="483e7-106">PSServiceDiagnosticSettings objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="483e7-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="483e7-107">Ez paraméterként használható a `-InputObject``Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="483e7-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="483e7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="483e7-108">EXAMPLES</span></span>

### <span data-ttu-id="483e7-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="483e7-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="483e7-110">PSServiceDiagnosticSettings objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="483e7-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="483e7-111">És hozzon létre diagnosztikai beállításokat a célerőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="483e7-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="483e7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="483e7-112">PARAMETERS</span></span>

### <span data-ttu-id="483e7-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="483e7-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="483e7-114">Az az érték, amely azt jelzi, hogy az exportálás (ODS-fájlba) erőforrás-specifikus (ha van) vagy AzureDiagnostics szolgáltatásba (alapértelmezett, nincs jelen)</span><span class="sxs-lookup"><span data-stu-id="483e7-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483e7-115">-DefaultProfile</span></span>
<span data-ttu-id="483e7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="483e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="483e7-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="483e7-118">Az eseményközpont szabályazonosítója</span><span class="sxs-lookup"><span data-stu-id="483e7-118">The event hub rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="483e7-119">-EventHubName</span></span>
<span data-ttu-id="483e7-120">A szolgáltatásbusz szabályazonosítója</span><span class="sxs-lookup"><span data-stu-id="483e7-120">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="483e7-121">-Name</span></span>
<span data-ttu-id="483e7-122">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="483e7-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="483e7-123">Alapértékek a "szolgáltatás" beállításhoz</span><span class="sxs-lookup"><span data-stu-id="483e7-123">Defaults to 'service'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="483e7-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="483e7-125">A szolgáltatásbusz szabályazonosítója</span><span class="sxs-lookup"><span data-stu-id="483e7-125">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-126">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="483e7-126">-Setting</span></span>
<span data-ttu-id="483e7-127">Metrikus beállítások vagy naplóbeállítások</span><span class="sxs-lookup"><span data-stu-id="483e7-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="483e7-128">-StorageAccountId</span></span>
<span data-ttu-id="483e7-129">A tárfiók azonosítója</span><span class="sxs-lookup"><span data-stu-id="483e7-129">The storage account id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="483e7-130">-TargetResourceId</span></span>
<span data-ttu-id="483e7-131">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="483e7-131">The resource id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="483e7-132">-WorkspaceId</span></span>
<span data-ttu-id="483e7-133">A Naplóelemzés munkaterület erőforrás-azonosítója, amelybe naplókat/metrikákat kell küldeni</span><span class="sxs-lookup"><span data-stu-id="483e7-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483e7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483e7-134">CommonParameters</span></span>
<span data-ttu-id="483e7-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483e7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483e7-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="483e7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483e7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="483e7-137">INPUTS</span></span>

### <span data-ttu-id="483e7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="483e7-138">System.String</span></span>

### <span data-ttu-id="483e7-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="483e7-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="483e7-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span><span class="sxs-lookup"><span data-stu-id="483e7-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="483e7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="483e7-141">OUTPUTS</span></span>

### <span data-ttu-id="483e7-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="483e7-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="483e7-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="483e7-143">NOTES</span></span>

## <span data-ttu-id="483e7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="483e7-144">RELATED LINKS</span></span>
