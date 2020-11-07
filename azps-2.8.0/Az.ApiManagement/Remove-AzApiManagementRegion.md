---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: ca40a9b74dd92b7bcdecdde87e4763f044b3272f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667967"
---
# <span data-ttu-id="8de25-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8de25-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="8de25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8de25-102">SYNOPSIS</span></span>
<span data-ttu-id="8de25-103">Eltávolítja a meglévő központi telepítő régiót a PsApiManagement-példányból.</span><span class="sxs-lookup"><span data-stu-id="8de25-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="8de25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8de25-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8de25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8de25-105">DESCRIPTION</span></span>
<span data-ttu-id="8de25-106">A **Remove-AzApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** fájltípust eltávolítja egy **AdditionalRegions** -gyűjteményből, a **Microsoft. Azure. commands. ApiManagement. modellek. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="8de25-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="8de25-107">Ez a parancsmag nem módosítja magát a központi telepítőt, de frissíti a **PsApiManagement** -példányt a memóriában.</span><span class="sxs-lookup"><span data-stu-id="8de25-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="8de25-108">Az API-kezelés telepített példányának frissítéséhez adja át a módosított **PsApiManagementInstance** a **set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="8de25-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="8de25-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8de25-109">EXAMPLES</span></span>

### <span data-ttu-id="8de25-110">1. példa: régió eltávolítása PsApiManagement példányból</span><span class="sxs-lookup"><span data-stu-id="8de25-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="8de25-111">Ez a parancs eltávolítja a kelet-amerikai régiót a **PsApiManagement** példányból.</span><span class="sxs-lookup"><span data-stu-id="8de25-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="8de25-112">2. példa: régió eltávolítása PsApiManagement példányból parancsok sorozatával</span><span class="sxs-lookup"><span data-stu-id="8de25-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="8de25-113">Az első parancs az **PsApiManagement** példányát kapja a contoso nevű ContosoApi nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="8de25-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="8de25-114">A végleges parancs ezután eltávolítja a kelet-amerikai régiót az adott példányból, majd frissíti a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="8de25-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="8de25-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8de25-115">PARAMETERS</span></span>

### <span data-ttu-id="8de25-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8de25-116">-ApiManagement</span></span>
<span data-ttu-id="8de25-117">Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag eltávolítja a további központi terjesztési területet.</span><span class="sxs-lookup"><span data-stu-id="8de25-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="8de25-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de25-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="8de25-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="8de25-119">-Location</span></span>
<span data-ttu-id="8de25-120">A parancsmag által eltávolított régió helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8de25-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="8de25-121">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="8de25-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="8de25-122">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="8de25-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="8de25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de25-123">CommonParameters</span></span>
<span data-ttu-id="8de25-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8de25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de25-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8de25-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de25-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8de25-126">INPUTS</span></span>

### <span data-ttu-id="8de25-127">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8de25-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="8de25-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8de25-128">System.String</span></span>

## <span data-ttu-id="8de25-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8de25-129">OUTPUTS</span></span>

### <span data-ttu-id="8de25-130">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8de25-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8de25-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8de25-131">NOTES</span></span>

## <span data-ttu-id="8de25-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8de25-132">RELATED LINKS</span></span>

[<span data-ttu-id="8de25-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8de25-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="8de25-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8de25-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


