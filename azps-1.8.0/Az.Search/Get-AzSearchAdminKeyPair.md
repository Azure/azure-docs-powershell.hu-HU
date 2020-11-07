---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: cd944184f4691b3f88934afc3a7bd9132eb23fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669281"
---
# <span data-ttu-id="013b2-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="013b2-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="013b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="013b2-102">SYNOPSIS</span></span>
<span data-ttu-id="013b2-103">Megkapja az Azure Search szolgáltatás rendszergazdai kulcs párjait.</span><span class="sxs-lookup"><span data-stu-id="013b2-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="013b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="013b2-104">SYNTAX</span></span>

### <span data-ttu-id="013b2-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="013b2-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="013b2-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="013b2-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="013b2-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="013b2-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="013b2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="013b2-108">DESCRIPTION</span></span>
<span data-ttu-id="013b2-109">A **Get-AzSearchAdminKeyPair** parancsmag az Azure Search szolgáltatáshoz tartozó rendszergazdai kulcspárt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="013b2-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="013b2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="013b2-110">EXAMPLES</span></span>

### <span data-ttu-id="013b2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="013b2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="013b2-112">A példa az Azure Search szolgáltatáshoz tartozó rendszergazdai kulcspárt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="013b2-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="013b2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="013b2-113">PARAMETERS</span></span>

### <span data-ttu-id="013b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="013b2-114">-DefaultProfile</span></span>
<span data-ttu-id="013b2-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="013b2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="013b2-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="013b2-116">-ParentObject</span></span>
<span data-ttu-id="013b2-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="013b2-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="013b2-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="013b2-118">-ParentResourceId</span></span>
<span data-ttu-id="013b2-119">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="013b2-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="013b2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="013b2-120">-ResourceGroupName</span></span>
<span data-ttu-id="013b2-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="013b2-121">Resource Group name.</span></span>

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

### <span data-ttu-id="013b2-122">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="013b2-122">-ServiceName</span></span>
<span data-ttu-id="013b2-123">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="013b2-123">Search Service name.</span></span>

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

### <span data-ttu-id="013b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="013b2-124">CommonParameters</span></span>
<span data-ttu-id="013b2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="013b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="013b2-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="013b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="013b2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="013b2-127">INPUTS</span></span>

### <span data-ttu-id="013b2-128">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="013b2-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="013b2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="013b2-129">System.String</span></span>

## <span data-ttu-id="013b2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="013b2-130">OUTPUTS</span></span>

### <span data-ttu-id="013b2-131">Microsoft. Azure. commands. Management. Search. models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="013b2-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="013b2-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="013b2-132">NOTES</span></span>

## <span data-ttu-id="013b2-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="013b2-133">RELATED LINKS</span></span>

[<span data-ttu-id="013b2-134">Új – AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="013b2-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
