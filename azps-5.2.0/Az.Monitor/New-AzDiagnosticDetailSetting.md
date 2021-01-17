---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350873"
---
# <span data-ttu-id="2cb2e-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="2cb2e-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="2cb2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb2e-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span><span class="sxs-lookup"><span data-stu-id="2cb2e-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="2cb2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2cb2e-104">SYNTAX</span></span>

### <span data-ttu-id="2cb2e-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cb2e-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb2e-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cb2e-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cb2e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2cb2e-107">DESCRIPTION</span></span>
<span data-ttu-id="2cb2e-108">PSMetricSettings vagy PSLogSettings objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="2cb2e-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="2cb2e-109">Kategóriákat a `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="2cb2e-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="2cb2e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2cb2e-110">EXAMPLES</span></span>

### <span data-ttu-id="2cb2e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2cb2e-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="2cb2e-112">PSMetricSettings objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="2cb2e-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="2cb2e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2cb2e-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="2cb2e-114">PSLogSettings objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="2cb2e-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="2cb2e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cb2e-115">PARAMETERS</span></span>

### <span data-ttu-id="2cb2e-116">-Category</span><span class="sxs-lookup"><span data-stu-id="2cb2e-116">-Category</span></span>
<span data-ttu-id="2cb2e-117">A beállítás kategóriája</span><span class="sxs-lookup"><span data-stu-id="2cb2e-117">Category of setting</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb2e-118">-DefaultProfile</span></span>
<span data-ttu-id="2cb2e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb2e-120">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2cb2e-120">-Enabled</span></span>
<span data-ttu-id="2cb2e-121">A beállítás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="2cb2e-121">Enable the setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb2e-122">-Log</span><span class="sxs-lookup"><span data-stu-id="2cb2e-122">-Log</span></span>
<span data-ttu-id="2cb2e-123">Naplóbeállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="2cb2e-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb2e-124">-Metric</span><span class="sxs-lookup"><span data-stu-id="2cb2e-124">-Metric</span></span>
<span data-ttu-id="2cb2e-125">Metrikus beállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="2cb2e-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb2e-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="2cb2e-126">-RetentionEnabled</span></span>
<span data-ttu-id="2cb2e-127">Adatmegőrzési házirend engedélyezése</span><span class="sxs-lookup"><span data-stu-id="2cb2e-127">Enable Retention policy</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb2e-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2cb2e-128">-RetentionInDays</span></span>
<span data-ttu-id="2cb2e-129">Adatmegőrzési házirend adatmegőrzési napjai</span><span class="sxs-lookup"><span data-stu-id="2cb2e-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb2e-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="2cb2e-130">-TimeGrain</span></span>
<span data-ttu-id="2cb2e-131">TimeGrain for metric setting</span><span class="sxs-lookup"><span data-stu-id="2cb2e-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb2e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb2e-132">CommonParameters</span></span>
<span data-ttu-id="2cb2e-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb2e-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cb2e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb2e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cb2e-135">INPUTS</span></span>

### <span data-ttu-id="2cb2e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2cb2e-136">System.String</span></span>

## <span data-ttu-id="2cb2e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cb2e-137">OUTPUTS</span></span>

### <span data-ttu-id="2cb2e-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="2cb2e-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="2cb2e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2cb2e-139">NOTES</span></span>

## <span data-ttu-id="2cb2e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cb2e-140">RELATED LINKS</span></span>
