---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505859"
---
# <span data-ttu-id="73edc-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="73edc-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="73edc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73edc-102">SYNOPSIS</span></span>
<span data-ttu-id="73edc-103">Eltávolítja a meglévő központi telepítő régiót a PsApiManagement-példányból.</span><span class="sxs-lookup"><span data-stu-id="73edc-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73edc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73edc-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73edc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73edc-105">DESCRIPTION</span></span>
<span data-ttu-id="73edc-106">A **Remove-AzureRmApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** fájltípust eltávolítja egy **AdditionalRegions** -gyűjteményből, a **Microsoft. Azure. commands. ApiManagement. modellek. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="73edc-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="73edc-107">Ez a parancsmag nem módosítja magát a központi telepítőt, de frissíti a **PsApiManagement** -példányt a memóriában.</span><span class="sxs-lookup"><span data-stu-id="73edc-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="73edc-108">Az API-menedzsment telepített példányának frissítéséhez adja át a módosított **PsApiManagementInstance** a **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="73edc-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="73edc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="73edc-109">EXAMPLES</span></span>

### <span data-ttu-id="73edc-110">1. példa: régió eltávolítása PsApiManagement példányból</span><span class="sxs-lookup"><span data-stu-id="73edc-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="73edc-111">Ez a parancs eltávolítja a kelet-amerikai régiót a **PsApiManagement** példányból.</span><span class="sxs-lookup"><span data-stu-id="73edc-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="73edc-112">2. példa: régió eltávolítása PsApiManagement példányból parancsok sorozatával</span><span class="sxs-lookup"><span data-stu-id="73edc-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="73edc-113">Az első parancs az **PsApiManagement** példányát kapja a contoso nevű ContosoApi nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="73edc-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="73edc-114">A végleges parancs ezután eltávolítja a kelet-amerikai régiót az adott példányból, majd frissíti a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="73edc-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="73edc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73edc-115">PARAMETERS</span></span>

### <span data-ttu-id="73edc-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73edc-116">-ApiManagement</span></span>
<span data-ttu-id="73edc-117">Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag eltávolítja a további központi terjesztési területet.</span><span class="sxs-lookup"><span data-stu-id="73edc-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73edc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73edc-118">-DefaultProfile</span></span>
<span data-ttu-id="73edc-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73edc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="73edc-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="73edc-120">-Location</span></span>
<span data-ttu-id="73edc-121">A parancsmag által eltávolított régió helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73edc-121">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="73edc-122">Megadja az új központi üzembe helyezési terület helyét az API-kezelési szolgáltatás támogatott területe között.</span><span class="sxs-lookup"><span data-stu-id="73edc-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="73edc-123">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="73edc-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73edc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73edc-124">CommonParameters</span></span>
<span data-ttu-id="73edc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73edc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73edc-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73edc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73edc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73edc-127">INPUTS</span></span>

### <span data-ttu-id="73edc-128">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="73edc-128">PsApiManagement</span></span>
<span data-ttu-id="73edc-129">A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="73edc-129">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="73edc-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73edc-130">OUTPUTS</span></span>

### <span data-ttu-id="73edc-131">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="73edc-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="73edc-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73edc-132">NOTES</span></span>

## <span data-ttu-id="73edc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73edc-133">RELATED LINKS</span></span>

[<span data-ttu-id="73edc-134">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="73edc-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="73edc-135">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="73edc-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


