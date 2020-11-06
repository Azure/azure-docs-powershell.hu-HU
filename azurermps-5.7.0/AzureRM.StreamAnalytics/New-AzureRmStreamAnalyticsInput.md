---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d16b59ed089c4756cc83363f645bdd7c47bb7f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498672"
---
# <span data-ttu-id="62f07-101">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="62f07-101">New-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="62f07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62f07-102">SYNOPSIS</span></span>
<span data-ttu-id="62f07-103">Projekthez tartozó bevitelt hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="62f07-103">Creates or updates a job input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62f07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62f07-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62f07-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62f07-105">DESCRIPTION</span></span>
<span data-ttu-id="62f07-106">A **New-AzureRmStreamAnalyticsInput** parancsmag létrehoz egy bemenetet egy adatfolyam-elemzési munkafolyamaton belül, vagy egy meglévő bemenetet frissít.</span><span class="sxs-lookup"><span data-stu-id="62f07-106">The **New-AzureRmStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="62f07-107">A beviteli nevet a JSON-fájlban vagy a parancssorban lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="62f07-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="62f07-108">Ha a két érték van megadva, a parancssorban lévő név egyeznie kell a fájl nevével.</span><span class="sxs-lookup"><span data-stu-id="62f07-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="62f07-109">Ha olyan bemenetet ad meg, amely már létezik, és nem adja meg az *erő* paramétert, akkor a parancsmag azt fogja megkérdezni, hogy lecseréli-e a meglévő bemenetet.</span><span class="sxs-lookup"><span data-stu-id="62f07-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>

<span data-ttu-id="62f07-110">Ha az *erő* paramétert adja meg, és egy meglévő beviteli nevet ad meg, a program megerősítés nélkül lecseréli a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="62f07-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="62f07-111">Példák</span><span class="sxs-lookup"><span data-stu-id="62f07-111">EXAMPLES</span></span>

### <span data-ttu-id="62f07-112">1. példa: bevitt munka létrehozása egy definícióval egy fájlból</span><span class="sxs-lookup"><span data-stu-id="62f07-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="62f07-113">Ez a parancs a fájl Input.jsbeírását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="62f07-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="62f07-114">Ha már definiált egy meglévő bemenetet a szövegbeviteli definíciós fájlban megadott névvel, a parancsmag megkérdezi, hogy a program lecseréli-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="62f07-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="62f07-115">2. példa: projekt bemenetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="62f07-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="62f07-116">Ezzel a paranccsal új adatokat hozhat létre a EntryStream nevű feladathoz.</span><span class="sxs-lookup"><span data-stu-id="62f07-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="62f07-117">Ha már meg van határozva egy meglévő bemenet, akkor a parancsmag megkérdezi, hogy lecseréli-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="62f07-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="62f07-118">3. példa: a bevitt munka lecserélése egy definícióval egy fájlból</span><span class="sxs-lookup"><span data-stu-id="62f07-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="62f07-119">Ez a parancs felülírja a EntryStream nevű meglévő beviteli forrás definícióját a definíció fájlból megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="62f07-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="62f07-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62f07-120">PARAMETERS</span></span>

### <span data-ttu-id="62f07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f07-121">-DefaultProfile</span></span>
<span data-ttu-id="62f07-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62f07-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f07-123">-Fájl</span><span class="sxs-lookup"><span data-stu-id="62f07-123">-File</span></span>
<span data-ttu-id="62f07-124">Annak a JSON-fájlnak az elérési útját adja meg, amely az Azure stream Analytics által létrehozott bemenet JSON-beli képviseletét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="62f07-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f07-125">-Force</span><span class="sxs-lookup"><span data-stu-id="62f07-125">-Force</span></span>
<span data-ttu-id="62f07-126">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="62f07-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f07-127">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="62f07-127">-JobName</span></span>
<span data-ttu-id="62f07-128">Annak az Azure stream-elemzési projektnek a nevét adja meg, amely alatt az Azure stream Analytics-adatbevitel hozható létre.</span><span class="sxs-lookup"><span data-stu-id="62f07-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f07-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62f07-129">-Name</span></span>
<span data-ttu-id="62f07-130">A létrehozandó Azure stream Analytics-bemenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62f07-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f07-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f07-131">-ResourceGroupName</span></span>
<span data-ttu-id="62f07-132">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az Azure adatfolyam-bevitelt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="62f07-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f07-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62f07-133">-Confirm</span></span>
<span data-ttu-id="62f07-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62f07-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62f07-135">-WhatIf</span></span>
<span data-ttu-id="62f07-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62f07-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62f07-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62f07-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f07-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f07-138">CommonParameters</span></span>
<span data-ttu-id="62f07-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62f07-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f07-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f07-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f07-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62f07-141">INPUTS</span></span>

### <span data-ttu-id="62f07-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="62f07-142">None</span></span>
<span data-ttu-id="62f07-143">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="62f07-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62f07-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62f07-144">OUTPUTS</span></span>

### <span data-ttu-id="62f07-145">Microsoft. Azure. Command. StreamAnalytics. models. PSInput</span><span class="sxs-lookup"><span data-stu-id="62f07-145">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="62f07-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62f07-146">NOTES</span></span>

## <span data-ttu-id="62f07-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62f07-147">RELATED LINKS</span></span>

[<span data-ttu-id="62f07-148">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="62f07-148">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="62f07-149">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="62f07-149">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="62f07-150">Teszt-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="62f07-150">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


