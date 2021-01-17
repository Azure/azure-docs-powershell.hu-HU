---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339798"
---
# <span data-ttu-id="b2c4d-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b2c4d-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="b2c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c4d-103">Eltávolít egy meglévő telepítési régiót a PsApiManagement-példányból.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="b2c4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2c4d-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2c4d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c4d-106">A **Remove-AzApiManagementRegion** parancsmag eltávolítja a **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** típusú példányokat az **AdditionalRegions** gyűjteményből, feltéve hogy a **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="b2c4d-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="b2c4d-107">Ez a parancsmag nem módosítja a telepítést önmagában, de frissíti a **PsApiManagement** in-memory példányát.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="b2c4d-108">Az API-felügyelet telepítésének frissítéséhez adja át a **módosított PsApiManagementInstance-t** a **Set-AzApiManagementnek.**</span><span class="sxs-lookup"><span data-stu-id="b2c4d-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="b2c4d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2c4d-109">EXAMPLES</span></span>

### <span data-ttu-id="b2c4d-110">1. példa: Régió eltávolítása a PsApiManagement-példányból</span><span class="sxs-lookup"><span data-stu-id="b2c4d-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="b2c4d-111">Ez a parancs eltávolítja az Egyesült Államok keleti régióját a **PsApiManagement-példányból.**</span><span class="sxs-lookup"><span data-stu-id="b2c4d-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="b2c4d-112">2. példa: Terület eltávolítása a PsApiManagement-példányból parancssorozat használatával</span><span class="sxs-lookup"><span data-stu-id="b2c4d-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="b2c4d-113">Ez az első parancs a ContosoApi nevű erőforráscsoport **PsApiManagement** példányát kapja.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="b2c4d-114">Az utolsó parancs ezután eltávolítja az Egyesült Államok keleti régióját a példányból, majd frissíti az üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="b2c4d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2c4d-115">PARAMETERS</span></span>

### <span data-ttu-id="b2c4d-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b2c4d-116">-ApiManagement</span></span>
<span data-ttu-id="b2c4d-117">Azt a **PsApiManagement-példányt** adja meg, amelyből a parancsmag eltávolítja a további telepítési régiót.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4d-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="b2c4d-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b2c4d-119">-Location</span></span>
<span data-ttu-id="b2c4d-120">Megadja annak a területnek a helyét, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="b2c4d-121">Megadja az új telepítési régió helyét az Api Management szolgáltatás támogatott régiója között.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="b2c4d-122">Érvényes helyek beszerzéséhez használja a Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" parancsmagot | ahol {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="b2c4d-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c4d-123">CommonParameters</span></span>
<span data-ttu-id="b2c4d-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c4d-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2c4d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c4d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2c4d-126">INPUTS</span></span>

### <span data-ttu-id="b2c4d-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b2c4d-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="b2c4d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b2c4d-128">System.String</span></span>

## <span data-ttu-id="b2c4d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2c4d-129">OUTPUTS</span></span>

### <span data-ttu-id="b2c4d-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b2c4d-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b2c4d-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2c4d-131">NOTES</span></span>

## <span data-ttu-id="b2c4d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2c4d-132">RELATED LINKS</span></span>

[<span data-ttu-id="b2c4d-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b2c4d-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="b2c4d-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b2c4d-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


