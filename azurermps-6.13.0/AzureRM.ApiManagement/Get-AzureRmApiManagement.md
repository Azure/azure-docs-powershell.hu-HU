---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: bff36b7bcb37dd099f9aa50a99bed9538111e8d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502287"
---
# <span data-ttu-id="c6870-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6870-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="c6870-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6870-102">SYNOPSIS</span></span>
<span data-ttu-id="c6870-103">Listát vagy API-kezelési szolgáltatás leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="c6870-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6870-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6870-104">SYNTAX</span></span>

### <span data-ttu-id="c6870-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6870-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6870-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6870-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6870-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="c6870-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6870-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6870-108">DESCRIPTION</span></span>
<span data-ttu-id="c6870-109">A **Get-AzureRmApiManagement** parancsmag felsorolja az összes API-kezelési szolgáltatást az előfizetés vagy a megadott erőforráscsoport vagy egy bizonyos API-kezelés csoportban.</span><span class="sxs-lookup"><span data-stu-id="c6870-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="c6870-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c6870-110">EXAMPLES</span></span>

### <span data-ttu-id="c6870-111">Példa 1: az API-kezelési szolgáltatások beszerzése</span><span class="sxs-lookup"><span data-stu-id="c6870-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="c6870-112">Ez a parancs az összes API-kezelési szolgáltatást beilleszti az előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="c6870-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="c6870-113">2. példa: az API-kezelési szolgáltatások beszerzése egy adott névvel</span><span class="sxs-lookup"><span data-stu-id="c6870-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="c6870-114">Ez a parancs a minden API-kezelési szolgáltatás bekerül a név mezőbe.</span><span class="sxs-lookup"><span data-stu-id="c6870-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="c6870-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6870-115">PARAMETERS</span></span>

### <span data-ttu-id="c6870-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6870-116">-DefaultProfile</span></span>
<span data-ttu-id="c6870-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6870-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6870-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6870-118">-Name</span></span>
<span data-ttu-id="c6870-119">Az API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6870-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6870-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6870-120">-ResourceGroupName</span></span>
<span data-ttu-id="c6870-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyben a parancsmag az API-kezelési szolgáltatást kapja.</span><span class="sxs-lookup"><span data-stu-id="c6870-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6870-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6870-122">CommonParameters</span></span>
<span data-ttu-id="c6870-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6870-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6870-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6870-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6870-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6870-125">INPUTS</span></span>

### <span data-ttu-id="c6870-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c6870-126">System.String</span></span>

## <span data-ttu-id="c6870-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6870-127">OUTPUTS</span></span>

### <span data-ttu-id="c6870-128">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6870-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c6870-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6870-129">NOTES</span></span>

## <span data-ttu-id="c6870-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6870-130">RELATED LINKS</span></span>

[<span data-ttu-id="c6870-131">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6870-131">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="c6870-132">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6870-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="c6870-133">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6870-133">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="c6870-134">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6870-134">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


