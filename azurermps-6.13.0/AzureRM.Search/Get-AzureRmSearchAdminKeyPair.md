---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
ms.openlocfilehash: 92b2e7304c0f837e47f7464e84769478902c973a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499419"
---
# <span data-ttu-id="d2ec6-101">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="d2ec6-101">Get-AzureRmSearchAdminKeyPair</span></span>

## <span data-ttu-id="d2ec6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ec6-103">Megkapja az Azure Search szolgáltatás rendszergazdai kulcs párjait.</span><span class="sxs-lookup"><span data-stu-id="d2ec6-103">Gets admin key pair of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2ec6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2ec6-104">SYNTAX</span></span>

### <span data-ttu-id="d2ec6-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2ec6-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2ec6-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2ec6-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2ec6-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2ec6-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2ec6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2ec6-108">DESCRIPTION</span></span>
<span data-ttu-id="d2ec6-109">A **Get-AzureRmSearchAdminKeyPair** parancsmag az Azure Search szolgáltatáshoz tartozó rendszergazdai kulcspárt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2ec6-109">The **Get-AzureRmSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="d2ec6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d2ec6-110">EXAMPLES</span></span>

### <span data-ttu-id="d2ec6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d2ec6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="d2ec6-112">A példa az Azure Search szolgáltatáshoz tartozó rendszergazdai kulcspárt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2ec6-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="d2ec6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2ec6-113">PARAMETERS</span></span>

### <span data-ttu-id="d2ec6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ec6-114">-DefaultProfile</span></span>
<span data-ttu-id="d2ec6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2ec6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2ec6-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d2ec6-116">-ParentObject</span></span>
<span data-ttu-id="d2ec6-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="d2ec6-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec6-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d2ec6-118">-ParentResourceId</span></span>
<span data-ttu-id="d2ec6-119">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d2ec6-119">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ec6-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2ec6-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d2ec6-121">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec6-122">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="d2ec6-122">-ServiceName</span></span>
<span data-ttu-id="d2ec6-123">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="d2ec6-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ec6-124">CommonParameters</span></span>
<span data-ttu-id="d2ec6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2ec6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ec6-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ec6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ec6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2ec6-127">INPUTS</span></span>

### <span data-ttu-id="d2ec6-128">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d2ec6-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="d2ec6-129">Paraméterek: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2ec6-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="d2ec6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ec6-130">System.String</span></span>

## <span data-ttu-id="d2ec6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2ec6-131">OUTPUTS</span></span>

### <span data-ttu-id="d2ec6-132">Microsoft. Azure. commands. Management. Search. models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="d2ec6-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="d2ec6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2ec6-133">NOTES</span></span>

## <span data-ttu-id="d2ec6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2ec6-134">RELATED LINKS</span></span>

[<span data-ttu-id="d2ec6-135">Új – AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="d2ec6-135">New-AzureRmSearchAdminKey</span></span>](./New-AzureRmSearchAdminKey.md)
