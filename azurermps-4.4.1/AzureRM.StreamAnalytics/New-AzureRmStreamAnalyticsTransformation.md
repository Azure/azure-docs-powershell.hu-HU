---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: eb9f8b82e8ff8a0f60931953f2a3b4349e7b4a4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494594"
---
# <span data-ttu-id="e7fec-101">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="e7fec-101">New-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="e7fec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7fec-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fec-103">Átalakulást hoz létre vagy frissít a projekten belül.</span><span class="sxs-lookup"><span data-stu-id="e7fec-103">Creates or updates a transformation within a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7fec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7fec-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7fec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7fec-105">DESCRIPTION</span></span>
<span data-ttu-id="e7fec-106">A **New-AzureRmStreamAnalyticsTransformation** parancsmag átalakulást hoz létre egy adatfolyam-elemzési munkafolyamaton belül, vagy frissíti a meglévő átalakítást.</span><span class="sxs-lookup"><span data-stu-id="e7fec-106">The **New-AzureRmStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="e7fec-107">Az átalakítás neve megadható. JSON-fájl vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="e7fec-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="e7fec-108">Ha a két érték van megadva, a parancssorban lévő név egyeznie kell a fájl nevével.</span><span class="sxs-lookup"><span data-stu-id="e7fec-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="e7fec-109">Ha olyan átalakítást ad meg, amely már létezik, és nem adja meg az erő paramétert, akkor a parancsmag azt fogja megkérdezni, hogy lecseréli-e a meglévő átalakítást.</span><span class="sxs-lookup"><span data-stu-id="e7fec-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>

<span data-ttu-id="e7fec-110">Ha az *erő* paramétert adja meg, és egy meglévő átalakítási nevet ad meg, az átalakítás megerősítés nélkül megszűnik.</span><span class="sxs-lookup"><span data-stu-id="e7fec-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="e7fec-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e7fec-111">EXAMPLES</span></span>

### <span data-ttu-id="e7fec-112">1. példa: átalakítás létrehozása vagy cseréje a projektben</span><span class="sxs-lookup"><span data-stu-id="e7fec-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="e7fec-113">Ez a parancs létrehoz egy StreamingJobTransform nevű átalakítást a StreamingJob nevű munkában.</span><span class="sxs-lookup"><span data-stu-id="e7fec-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="e7fec-114">Ha egy meglévő átalakítás már definiálva van az adott névvel, a parancsmag azt fogja megkérdezni, hogy lecseréli-e.</span><span class="sxs-lookup"><span data-stu-id="e7fec-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="e7fec-115">2. példa: átalakítás cseréje a projektben</span><span class="sxs-lookup"><span data-stu-id="e7fec-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="e7fec-116">Ez a parancs a StreamingJobTransform definícióját lecseréli a feladat StreamingJob megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="e7fec-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="e7fec-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7fec-117">PARAMETERS</span></span>

### <span data-ttu-id="e7fec-118">-Fájl</span><span class="sxs-lookup"><span data-stu-id="e7fec-118">-File</span></span>
<span data-ttu-id="e7fec-119">Annak a JSON-fájlnak az elérési útját adja meg, amely az Azure stream Analytics transzformációjának JSON-ábrázolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e7fec-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="e7fec-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e7fec-120">-Force</span></span>
<span data-ttu-id="e7fec-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e7fec-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7fec-122">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="e7fec-122">-JobName</span></span>
<span data-ttu-id="e7fec-123">Annak az Azure stream Analytics-feladatnak a nevét adja meg, amely alatt az Azure stream Analytics-átalakítót létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="e7fec-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="e7fec-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7fec-124">-Name</span></span>
<span data-ttu-id="e7fec-125">A létrehozandó Azure stream Analytics-transzformáció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7fec-125">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="e7fec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7fec-126">-ResourceGroupName</span></span>
<span data-ttu-id="e7fec-127">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az Azure stream Analytics-transzformációt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="e7fec-127">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="e7fec-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7fec-128">-Confirm</span></span>
<span data-ttu-id="e7fec-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7fec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7fec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7fec-130">-WhatIf</span></span>
<span data-ttu-id="e7fec-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7fec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7fec-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7fec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7fec-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fec-133">-DefaultProfile</span></span>
<span data-ttu-id="e7fec-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7fec-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fec-135">CommonParameters</span></span>
<span data-ttu-id="e7fec-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7fec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fec-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7fec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fec-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7fec-138">INPUTS</span></span>

## <span data-ttu-id="e7fec-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7fec-139">OUTPUTS</span></span>

### <span data-ttu-id="e7fec-140">Microsoft. Azure. Command. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="e7fec-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="e7fec-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7fec-141">NOTES</span></span>

## <span data-ttu-id="e7fec-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7fec-142">RELATED LINKS</span></span>

[<span data-ttu-id="e7fec-143">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="e7fec-143">Get-AzureRmStreamAnalyticsTransformation</span></span>](./Get-AzureRmStreamAnalyticsTransformation.md)


