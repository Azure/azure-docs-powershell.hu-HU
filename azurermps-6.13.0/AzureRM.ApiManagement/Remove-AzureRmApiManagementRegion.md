---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ccd7379a07b83b3ed45eff5f8095b950868810c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679218"
---
# <span data-ttu-id="da07e-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="da07e-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="da07e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da07e-102">SYNOPSIS</span></span>
<span data-ttu-id="da07e-103">Eltávolítja a meglévő központi telepítő régiót a PsApiManagement-példányból.</span><span class="sxs-lookup"><span data-stu-id="da07e-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da07e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da07e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da07e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da07e-105">DESCRIPTION</span></span>
<span data-ttu-id="da07e-106">A **Remove-AzureRmApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** fájltípust eltávolítja egy **AdditionalRegions** -gyűjteményből, a **Microsoft. Azure. commands. ApiManagement. modellek. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="da07e-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="da07e-107">Ez a parancsmag nem módosítja magát a központi telepítőt, de frissíti a **PsApiManagement** -példányt a memóriában.</span><span class="sxs-lookup"><span data-stu-id="da07e-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="da07e-108">Az API-menedzsment telepített példányának frissítéséhez adja át a módosított **PsApiManagementInstance** a **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="da07e-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="da07e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="da07e-109">EXAMPLES</span></span>

### <span data-ttu-id="da07e-110">1. példa: régió eltávolítása PsApiManagement példányból</span><span class="sxs-lookup"><span data-stu-id="da07e-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="da07e-111">Ez a parancs eltávolítja a kelet-amerikai régiót a **PsApiManagement** példányból.</span><span class="sxs-lookup"><span data-stu-id="da07e-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="da07e-112">2. példa: régió eltávolítása PsApiManagement példányból parancsok sorozatával</span><span class="sxs-lookup"><span data-stu-id="da07e-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="da07e-113">Az első parancs az **PsApiManagement** példányát kapja a contoso nevű ContosoApi nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="da07e-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="da07e-114">A végleges parancs ezután eltávolítja a kelet-amerikai régiót az adott példányból, majd frissíti a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="da07e-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="da07e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da07e-115">PARAMETERS</span></span>

### <span data-ttu-id="da07e-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="da07e-116">-ApiManagement</span></span>
<span data-ttu-id="da07e-117">Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag eltávolítja a további központi terjesztési területet.</span><span class="sxs-lookup"><span data-stu-id="da07e-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="da07e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da07e-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="da07e-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="da07e-119">-Location</span></span>
<span data-ttu-id="da07e-120">A parancsmag által eltávolított régió helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da07e-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="da07e-121">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="da07e-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="da07e-122">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="da07e-122">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="da07e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da07e-123">CommonParameters</span></span>
<span data-ttu-id="da07e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da07e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da07e-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da07e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da07e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da07e-126">INPUTS</span></span>

### <span data-ttu-id="da07e-127">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="da07e-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="da07e-128">Paraméterek: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="da07e-128">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="da07e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="da07e-129">System.String</span></span>

## <span data-ttu-id="da07e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da07e-130">OUTPUTS</span></span>

### <span data-ttu-id="da07e-131">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="da07e-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="da07e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da07e-132">NOTES</span></span>

## <span data-ttu-id="da07e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da07e-133">RELATED LINKS</span></span>

[<span data-ttu-id="da07e-134">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="da07e-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="da07e-135">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="da07e-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


