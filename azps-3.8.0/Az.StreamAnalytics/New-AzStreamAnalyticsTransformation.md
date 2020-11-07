---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 833ad7d57259d9a1f308c676ba49a93935d7e045
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845165"
---
# <span data-ttu-id="57109-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="57109-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="57109-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57109-102">SYNOPSIS</span></span>
<span data-ttu-id="57109-103">Átalakulást hoz létre vagy frissít a projekten belül.</span><span class="sxs-lookup"><span data-stu-id="57109-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="57109-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57109-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57109-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57109-105">DESCRIPTION</span></span>
<span data-ttu-id="57109-106">A **New-AzStreamAnalyticsTransformation** parancsmag átalakulást hoz létre egy adatfolyam-elemzési munkafolyamaton belül, vagy frissíti a meglévő átalakítást.</span><span class="sxs-lookup"><span data-stu-id="57109-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="57109-107">Az átalakítás neve megadható. JSON-fájl vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="57109-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="57109-108">Ha a két érték van megadva, a parancssorban lévő név egyeznie kell a fájl nevével.</span><span class="sxs-lookup"><span data-stu-id="57109-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="57109-109">Ha olyan átalakítást ad meg, amely már létezik, és nem adja meg az erő paramétert, akkor a parancsmag azt fogja megkérdezni, hogy lecseréli-e a meglévő átalakítást.</span><span class="sxs-lookup"><span data-stu-id="57109-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="57109-110">Ha az *erő* paramétert adja meg, és egy meglévő átalakítási nevet ad meg, az átalakítás megerősítés nélkül megszűnik.</span><span class="sxs-lookup"><span data-stu-id="57109-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="57109-111">Példák</span><span class="sxs-lookup"><span data-stu-id="57109-111">EXAMPLES</span></span>

### <span data-ttu-id="57109-112">1. példa: átalakítás létrehozása vagy cseréje a projektben</span><span class="sxs-lookup"><span data-stu-id="57109-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="57109-113">Ez a parancs létrehoz egy StreamingJobTransform nevű átalakítást a StreamingJob nevű munkában.</span><span class="sxs-lookup"><span data-stu-id="57109-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="57109-114">Ha egy meglévő átalakítás már definiálva van az adott névvel, a parancsmag azt fogja megkérdezni, hogy lecseréli-e.</span><span class="sxs-lookup"><span data-stu-id="57109-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="57109-115">2. példa: átalakítás cseréje a projektben</span><span class="sxs-lookup"><span data-stu-id="57109-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="57109-116">Ez a parancs a StreamingJobTransform definícióját lecseréli a feladat StreamingJob megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="57109-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="57109-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57109-117">PARAMETERS</span></span>

### <span data-ttu-id="57109-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57109-118">-DefaultProfile</span></span>
<span data-ttu-id="57109-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57109-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57109-120">-Fájl</span><span class="sxs-lookup"><span data-stu-id="57109-120">-File</span></span>
<span data-ttu-id="57109-121">Annak a JSON-fájlnak az elérési útját adja meg, amely az Azure stream Analytics transzformációjának JSON-ábrázolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="57109-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57109-122">-Force</span><span class="sxs-lookup"><span data-stu-id="57109-122">-Force</span></span>
<span data-ttu-id="57109-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="57109-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57109-124">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="57109-124">-JobName</span></span>
<span data-ttu-id="57109-125">Annak az Azure stream Analytics-feladatnak a nevét adja meg, amely alatt az Azure stream Analytics-átalakítót létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="57109-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57109-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57109-126">-Name</span></span>
<span data-ttu-id="57109-127">A létrehozandó Azure stream Analytics-transzformáció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57109-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57109-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57109-128">-ResourceGroupName</span></span>
<span data-ttu-id="57109-129">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az Azure stream Analytics-transzformációt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="57109-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57109-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57109-130">-Confirm</span></span>
<span data-ttu-id="57109-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57109-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57109-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57109-132">-WhatIf</span></span>
<span data-ttu-id="57109-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57109-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57109-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57109-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57109-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57109-135">CommonParameters</span></span>
<span data-ttu-id="57109-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57109-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57109-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57109-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57109-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57109-138">INPUTS</span></span>

### <span data-ttu-id="57109-139">System. String</span><span class="sxs-lookup"><span data-stu-id="57109-139">System.String</span></span>

## <span data-ttu-id="57109-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57109-140">OUTPUTS</span></span>

### <span data-ttu-id="57109-141">Microsoft. Azure. Command. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="57109-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="57109-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57109-142">NOTES</span></span>

## <span data-ttu-id="57109-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57109-143">RELATED LINKS</span></span>

[<span data-ttu-id="57109-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="57109-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


