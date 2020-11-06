---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: f2d9d2b53d07380e3bdb0a97ea3f3e70107ee0a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494596"
---
# <span data-ttu-id="c4897-101">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c4897-101">New-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="c4897-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4897-102">SYNOPSIS</span></span>
<span data-ttu-id="c4897-103">Kimeneteket hoz létre vagy frissít egy adatfolyam-elemzési feladathoz.</span><span class="sxs-lookup"><span data-stu-id="c4897-103">Creates or updates outputs for a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4897-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4897-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4897-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4897-105">DESCRIPTION</span></span>
<span data-ttu-id="c4897-106">A **New-AzureRmStreamAnalyticsOutput** parancsmag kimenetet hoz létre egy adatfolyam-elemzési munkafolyamaton belül, vagy egy meglévő kimenetet frissít.</span><span class="sxs-lookup"><span data-stu-id="c4897-106">The **New-AzureRmStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="c4897-107">A kimenet neve megadható a mezőben. JSON-fájl vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="c4897-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="c4897-108">Ha a két érték van megadva, a parancssorban lévő név egyeznie kell a fájl nevével.</span><span class="sxs-lookup"><span data-stu-id="c4897-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="c4897-109">Ha olyan kimenetet ad meg, amely már létezik, és nem adja meg az *erő* paramétert, a parancsmag azt fogja megkérdezni, hogy a meglévő kimenetet szeretné-e cserélni.</span><span class="sxs-lookup"><span data-stu-id="c4897-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>

<span data-ttu-id="c4897-110">Ha megadja az *erő* paramétert, és egy meglévő kimeneti nevet ad meg, a program megerősítés nélkül lecseréli a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c4897-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="c4897-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c4897-111">EXAMPLES</span></span>

### <span data-ttu-id="c4897-112">1. példa: kimenet hozzáadása a projekthez</span><span class="sxs-lookup"><span data-stu-id="c4897-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="c4897-113">Ezzel a paranccsal létrehoz egy új kimenet nevű kimenetet a StreamingJob nevű feladatba.</span><span class="sxs-lookup"><span data-stu-id="c4897-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="c4897-114">Ha már meg van határozva egy meglévő kimenet, akkor a parancsmag azt fogja megkérdezni, hogy lecseréli-e.</span><span class="sxs-lookup"><span data-stu-id="c4897-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="c4897-115">2. példa: a projekt kimeneti definíciójának cseréje</span><span class="sxs-lookup"><span data-stu-id="c4897-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="c4897-116">A parancs felülírja a StreamingJob nevű feladat kimenetének definícióját megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="c4897-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="c4897-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4897-117">PARAMETERS</span></span>

### <span data-ttu-id="c4897-118">-Fájl</span><span class="sxs-lookup"><span data-stu-id="c4897-118">-File</span></span>
<span data-ttu-id="c4897-119">Annak a JSON-fájlnak az elérési útját adja meg, amely az Azure stream Analytics kimenetének JSON-ábrázolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c4897-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="c4897-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c4897-120">-Force</span></span>
<span data-ttu-id="c4897-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c4897-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4897-122">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="c4897-122">-JobName</span></span>
<span data-ttu-id="c4897-123">Annak az Azure stream Analytics-feladatnak a nevét adja meg, amely alatt az Azure stream Analytics kimenete hozható létre.</span><span class="sxs-lookup"><span data-stu-id="c4897-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="c4897-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4897-124">-Name</span></span>
<span data-ttu-id="c4897-125">A létrehozandó Azure stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4897-125">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="c4897-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4897-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4897-127">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt létrehozhatja az Azure stream Analytics kimenetét.</span><span class="sxs-lookup"><span data-stu-id="c4897-127">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="c4897-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c4897-128">-Confirm</span></span>
<span data-ttu-id="c4897-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c4897-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4897-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4897-130">-WhatIf</span></span>
<span data-ttu-id="c4897-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c4897-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4897-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4897-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4897-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4897-133">-DefaultProfile</span></span>
<span data-ttu-id="c4897-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4897-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4897-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4897-135">CommonParameters</span></span>
<span data-ttu-id="c4897-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4897-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4897-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4897-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4897-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4897-138">INPUTS</span></span>

## <span data-ttu-id="c4897-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4897-139">OUTPUTS</span></span>

### <span data-ttu-id="c4897-140">Microsoft. Azure. Command. StreamAnalytics. models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="c4897-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="c4897-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4897-141">NOTES</span></span>

## <span data-ttu-id="c4897-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4897-142">RELATED LINKS</span></span>

[<span data-ttu-id="c4897-143">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c4897-143">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="c4897-144">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c4897-144">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="c4897-145">Teszt-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c4897-145">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


