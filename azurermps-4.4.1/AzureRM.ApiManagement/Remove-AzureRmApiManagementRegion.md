---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492597"
---
# <span data-ttu-id="21426-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="21426-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="21426-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21426-102">SYNOPSIS</span></span>
<span data-ttu-id="21426-103">Eltávolítja a meglévő központi telepítő régiót a PsApiManagement-példányból.</span><span class="sxs-lookup"><span data-stu-id="21426-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21426-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21426-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21426-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="21426-105">DESCRIPTION</span></span>
<span data-ttu-id="21426-106">A **Remove-AzureRmApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** fájltípust eltávolítja egy **AdditionalRegions** -gyűjteményből, a **Microsoft. Azure. commands. ApiManagement. modellek. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="21426-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="21426-107">Ez a parancsmag nem módosítja magát a központi telepítőt, de frissíti a **PsApiManagement** -példányt a memóriában.</span><span class="sxs-lookup"><span data-stu-id="21426-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="21426-108">Az API-menedzsment telepített példányának frissítéséhez adja át a módosított **PsApiManagementInstance** a **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="21426-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="21426-109">Példák</span><span class="sxs-lookup"><span data-stu-id="21426-109">EXAMPLES</span></span>

### <span data-ttu-id="21426-110">1. példa: régió eltávolítása PsApiManagement példányból</span><span class="sxs-lookup"><span data-stu-id="21426-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="21426-111">Ez a parancs eltávolítja a kelet-amerikai régiót a **PsApiManagement** példányból.</span><span class="sxs-lookup"><span data-stu-id="21426-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="21426-112">2. példa: régió eltávolítása PsApiManagement példányból parancsok sorozatával</span><span class="sxs-lookup"><span data-stu-id="21426-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="21426-113">Az első parancs az **PsApiManagement** példányát kapja a contoso nevű ContosoApi nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="21426-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="21426-114">A végleges parancs ezután eltávolítja a kelet-amerikai régiót az adott példányból, majd frissíti a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="21426-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="21426-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21426-115">PARAMETERS</span></span>

### <span data-ttu-id="21426-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="21426-116">-ApiManagement</span></span>
<span data-ttu-id="21426-117">Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag eltávolítja a további központi terjesztési területet.</span><span class="sxs-lookup"><span data-stu-id="21426-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="21426-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="21426-118">-Location</span></span>
<span data-ttu-id="21426-119">A parancsmag által eltávolított régió helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21426-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="21426-120">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="21426-120">Valid values are:</span></span> 

- <span data-ttu-id="21426-121">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="21426-121">North Central US</span></span>
- <span data-ttu-id="21426-122">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="21426-122">South Central US</span></span>
- <span data-ttu-id="21426-123">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="21426-123">Central US</span></span>
- <span data-ttu-id="21426-124">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="21426-124">West Europe</span></span>
- <span data-ttu-id="21426-125">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="21426-125">North Europe</span></span>
- <span data-ttu-id="21426-126">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="21426-126">West US</span></span>
- <span data-ttu-id="21426-127">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="21426-127">East US</span></span>
- <span data-ttu-id="21426-128">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="21426-128">East US 2</span></span>
- <span data-ttu-id="21426-129">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="21426-129">Japan East</span></span>
- <span data-ttu-id="21426-130">Japán West</span><span class="sxs-lookup"><span data-stu-id="21426-130">Japan West</span></span>
- <span data-ttu-id="21426-131">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="21426-131">Brazil South</span></span>
- <span data-ttu-id="21426-132">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="21426-132">Southeast Asia</span></span>
- <span data-ttu-id="21426-133">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="21426-133">East Asia</span></span>
- <span data-ttu-id="21426-134">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="21426-134">Australia East</span></span>
- <span data-ttu-id="21426-135">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="21426-135">Australia Southeast</span></span>

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

### <span data-ttu-id="21426-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21426-136">-DefaultProfile</span></span>
<span data-ttu-id="21426-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21426-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21426-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21426-138">CommonParameters</span></span>
<span data-ttu-id="21426-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21426-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21426-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21426-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21426-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21426-141">INPUTS</span></span>

### <span data-ttu-id="21426-142">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="21426-142">PsApiManagement</span></span>
<span data-ttu-id="21426-143">A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="21426-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="21426-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21426-144">OUTPUTS</span></span>

### <span data-ttu-id="21426-145">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="21426-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="21426-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21426-146">NOTES</span></span>

## <span data-ttu-id="21426-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21426-147">RELATED LINKS</span></span>

[<span data-ttu-id="21426-148">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="21426-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="21426-149">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="21426-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


