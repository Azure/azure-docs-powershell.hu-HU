---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: f8923c6f98dad44a56c35cadc4b3e1daedeb1227
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500012"
---
# <span data-ttu-id="b872a-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="b872a-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="b872a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b872a-102">SYNOPSIS</span></span>
<span data-ttu-id="b872a-103">A webszolgáltatás-definíciós objektumot JSON formátumú karakterláncként exportálja.</span><span class="sxs-lookup"><span data-stu-id="b872a-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b872a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b872a-104">SYNTAX</span></span>

### <span data-ttu-id="b872a-105">Exportálás fájlba lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="b872a-105">Export to file.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b872a-106">Exportálás JSON-karakterláncba</span><span class="sxs-lookup"><span data-stu-id="b872a-106">Export to JSON string.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b872a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b872a-107">DESCRIPTION</span></span>
<span data-ttu-id="b872a-108">A megadott webszolga definíciós objektumának exportálása JSON formátumú karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="b872a-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="b872a-109">A karakterláncot azonnal visszaállíthatja, vagy fájlba mentheti.</span><span class="sxs-lookup"><span data-stu-id="b872a-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="b872a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b872a-110">EXAMPLES</span></span>

### <span data-ttu-id="b872a-111">--------------------------Példa 1: exportálás karakterláncként--------------------------</span><span class="sxs-lookup"><span data-stu-id="b872a-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
<span data-ttu-id="b872a-112">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b872a-112">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="b872a-113">--------------------------Példa 2: Exportálás fájlba--------------------------</span><span class="sxs-lookup"><span data-stu-id="b872a-113">--------------------------  Example 2: Export to file  --------------------------</span></span>
<span data-ttu-id="b872a-114">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b872a-114">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="b872a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b872a-115">PARAMETERS</span></span>

### <span data-ttu-id="b872a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b872a-116">-Force</span></span>
<span data-ttu-id="b872a-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b872a-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b872a-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="b872a-118">-OutputFile</span></span>
<span data-ttu-id="b872a-119">Az exportált definíció fájlelérési útja.</span><span class="sxs-lookup"><span data-stu-id="b872a-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b872a-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="b872a-120">-ToJsonString</span></span>
<span data-ttu-id="b872a-121">Azt adja meg, hogy a definíció JSON-karakterláncként lesz exportálva.</span><span class="sxs-lookup"><span data-stu-id="b872a-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b872a-122">-Webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="b872a-122">-WebService</span></span>
<span data-ttu-id="b872a-123">Az exportálandó webszolgáltatás-definíciós objektum.</span><span class="sxs-lookup"><span data-stu-id="b872a-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b872a-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b872a-124">-Confirm</span></span>
<span data-ttu-id="b872a-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b872a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b872a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b872a-126">-WhatIf</span></span>
<span data-ttu-id="b872a-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b872a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b872a-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b872a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b872a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b872a-129">-DefaultProfile</span></span>
<span data-ttu-id="b872a-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b872a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b872a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b872a-131">CommonParameters</span></span>
<span data-ttu-id="b872a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b872a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b872a-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b872a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b872a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b872a-134">INPUTS</span></span>

### <span data-ttu-id="b872a-135">WebService</span><span class="sxs-lookup"><span data-stu-id="b872a-135">WebService</span></span>
<span data-ttu-id="b872a-136">A "webszolgáltatás" paraméter elfogadja a "webszolgáltatás" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b872a-136">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="b872a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b872a-137">OUTPUTS</span></span>

### <span data-ttu-id="b872a-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="b872a-138">None</span></span>

## <span data-ttu-id="b872a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b872a-139">NOTES</span></span>
<span data-ttu-id="b872a-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="b872a-140">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b872a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b872a-141">RELATED LINKS</span></span>

