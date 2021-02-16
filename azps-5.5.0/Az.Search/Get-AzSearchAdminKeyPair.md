---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: e6f2495392eed73e5576d8502f86a08e325337f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150843"
---
# <span data-ttu-id="d28c0-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="d28c0-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="d28c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d28c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d28c0-103">Az Azure Cognitive Search szolgáltatás rendszergazdai kulcspárt kap.</span><span class="sxs-lookup"><span data-stu-id="d28c0-103">Gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d28c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d28c0-104">SYNTAX</span></span>

### <span data-ttu-id="d28c0-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d28c0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d28c0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d28c0-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d28c0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d28c0-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d28c0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d28c0-108">DESCRIPTION</span></span>
<span data-ttu-id="d28c0-109">A **Get-AzSearchAdminKeyPair** parancsmag az Azure Kognitív keresés szolgáltatás rendszergazdai kulcspárt kap.</span><span class="sxs-lookup"><span data-stu-id="d28c0-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d28c0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d28c0-110">EXAMPLES</span></span>

### <span data-ttu-id="d28c0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d28c0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="d28c0-112">A példa az Azure Kognitív keresés szolgáltatás rendszergazdai kulcspárt kap.</span><span class="sxs-lookup"><span data-stu-id="d28c0-112">The example gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d28c0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d28c0-113">PARAMETERS</span></span>

### <span data-ttu-id="d28c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d28c0-114">-DefaultProfile</span></span>
<span data-ttu-id="d28c0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d28c0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d28c0-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d28c0-116">-ParentObject</span></span>
<span data-ttu-id="d28c0-117">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="d28c0-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="d28c0-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d28c0-118">-ParentResourceId</span></span>
<span data-ttu-id="d28c0-119">Azure Kognitív keresési szolgáltatás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d28c0-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d28c0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d28c0-120">-ResourceGroupName</span></span>
<span data-ttu-id="d28c0-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d28c0-121">Resource Group name.</span></span>

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

### <span data-ttu-id="d28c0-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d28c0-122">-ServiceName</span></span>
<span data-ttu-id="d28c0-123">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d28c0-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="d28c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d28c0-124">CommonParameters</span></span>
<span data-ttu-id="d28c0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d28c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d28c0-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d28c0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d28c0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d28c0-127">INPUTS</span></span>

### <span data-ttu-id="d28c0-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d28c0-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="d28c0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d28c0-129">System.String</span></span>

## <span data-ttu-id="d28c0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d28c0-130">OUTPUTS</span></span>

### <span data-ttu-id="d28c0-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="d28c0-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="d28c0-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d28c0-132">NOTES</span></span>

## <span data-ttu-id="d28c0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d28c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="d28c0-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="d28c0-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
