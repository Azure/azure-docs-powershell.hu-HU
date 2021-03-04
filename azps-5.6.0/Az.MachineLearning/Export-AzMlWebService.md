---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 0fad6a81f895643f8783ca8d179d68e31eed6da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931010"
---
# <span data-ttu-id="07bf5-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="07bf5-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="07bf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="07bf5-103">A webszolgáltatás-definíciós objektumot JSON formátumú karakterláncként exportálja.</span><span class="sxs-lookup"><span data-stu-id="07bf5-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="07bf5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07bf5-104">SYNTAX</span></span>

### <span data-ttu-id="07bf5-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="07bf5-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bf5-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="07bf5-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07bf5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07bf5-107">DESCRIPTION</span></span>
<span data-ttu-id="07bf5-108">A megadott webszolgáltatás definíciós objektumát JSON formátumú karakterláncként exportálja.</span><span class="sxs-lookup"><span data-stu-id="07bf5-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="07bf5-109">A karakterláncot azonnal vissza is használhatja, vagy mentheti egy fájlba.</span><span class="sxs-lookup"><span data-stu-id="07bf5-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="07bf5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07bf5-110">EXAMPLES</span></span>

### <span data-ttu-id="07bf5-111">1. példa: Exportálás karakterláncként</span><span class="sxs-lookup"><span data-stu-id="07bf5-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="07bf5-112">2. példa: Exportálás fájlba</span><span class="sxs-lookup"><span data-stu-id="07bf5-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="07bf5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07bf5-113">PARAMETERS</span></span>

### <span data-ttu-id="07bf5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bf5-114">-DefaultProfile</span></span>
<span data-ttu-id="07bf5-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="07bf5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07bf5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="07bf5-116">-Force</span></span>
<span data-ttu-id="07bf5-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07bf5-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="07bf5-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="07bf5-118">-OutputFile</span></span>
<span data-ttu-id="07bf5-119">Az exportált definíció fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="07bf5-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bf5-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="07bf5-120">-ToJsonString</span></span>
<span data-ttu-id="07bf5-121">Azt adja meg, hogy a definíció JSON-karakterláncként lesz exportálva.</span><span class="sxs-lookup"><span data-stu-id="07bf5-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bf5-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="07bf5-122">-WebService</span></span>
<span data-ttu-id="07bf5-123">Az exportálni célként használt webszolgáltatás-definíciós objektum.</span><span class="sxs-lookup"><span data-stu-id="07bf5-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="07bf5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07bf5-124">-Confirm</span></span>
<span data-ttu-id="07bf5-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07bf5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07bf5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bf5-126">-WhatIf</span></span>
<span data-ttu-id="07bf5-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07bf5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07bf5-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07bf5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07bf5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bf5-129">CommonParameters</span></span>
<span data-ttu-id="07bf5-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07bf5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bf5-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bf5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bf5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07bf5-132">INPUTS</span></span>

### <span data-ttu-id="07bf5-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="07bf5-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="07bf5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07bf5-134">OUTPUTS</span></span>

### <span data-ttu-id="07bf5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="07bf5-135">System.String</span></span>

## <span data-ttu-id="07bf5-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07bf5-136">NOTES</span></span>
<span data-ttu-id="07bf5-137">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="07bf5-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="07bf5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07bf5-138">RELATED LINKS</span></span>
