---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845821"
---
# <span data-ttu-id="43c23-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="43c23-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="43c23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43c23-102">SYNOPSIS</span></span>
<span data-ttu-id="43c23-103">Megkapja az Azure Search szolgáltatás rendszergazdai kulcs párjait.</span><span class="sxs-lookup"><span data-stu-id="43c23-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="43c23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43c23-104">SYNTAX</span></span>

### <span data-ttu-id="43c23-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43c23-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c23-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43c23-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43c23-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43c23-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43c23-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="43c23-108">DESCRIPTION</span></span>
<span data-ttu-id="43c23-109">A **Get-AzSearchAdminKeyPair** parancsmag az Azure Search szolgáltatáshoz tartozó rendszergazdai kulcspárt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="43c23-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="43c23-110">Példák</span><span class="sxs-lookup"><span data-stu-id="43c23-110">EXAMPLES</span></span>

### <span data-ttu-id="43c23-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43c23-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="43c23-112">A példa az Azure Search szolgáltatáshoz tartozó rendszergazdai kulcspárt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="43c23-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="43c23-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43c23-113">PARAMETERS</span></span>

### <span data-ttu-id="43c23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c23-114">-DefaultProfile</span></span>
<span data-ttu-id="43c23-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43c23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43c23-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="43c23-116">-ParentObject</span></span>
<span data-ttu-id="43c23-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="43c23-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="43c23-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="43c23-118">-ParentResourceId</span></span>
<span data-ttu-id="43c23-119">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="43c23-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="43c23-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c23-120">-ResourceGroupName</span></span>
<span data-ttu-id="43c23-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="43c23-121">Resource Group name.</span></span>

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

### <span data-ttu-id="43c23-122">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="43c23-122">-ServiceName</span></span>
<span data-ttu-id="43c23-123">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="43c23-123">Search Service name.</span></span>

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

### <span data-ttu-id="43c23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c23-124">CommonParameters</span></span>
<span data-ttu-id="43c23-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43c23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c23-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c23-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c23-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43c23-127">INPUTS</span></span>

### <span data-ttu-id="43c23-128">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="43c23-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="43c23-129">System. String</span><span class="sxs-lookup"><span data-stu-id="43c23-129">System.String</span></span>

## <span data-ttu-id="43c23-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43c23-130">OUTPUTS</span></span>

### <span data-ttu-id="43c23-131">Microsoft. Azure. commands. Management. Search. models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="43c23-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="43c23-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43c23-132">NOTES</span></span>

## <span data-ttu-id="43c23-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43c23-133">RELATED LINKS</span></span>

[<span data-ttu-id="43c23-134">Új – AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="43c23-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
