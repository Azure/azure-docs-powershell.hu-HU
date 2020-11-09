---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302018"
---
# <span data-ttu-id="e2b0d-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="e2b0d-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="e2b0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b0d-103">Személyes hivatkozás típusú erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-103">Gets a private link resource.</span></span>

## <span data-ttu-id="e2b0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2b0d-104">SYNTAX</span></span>

### <span data-ttu-id="e2b0d-105">ByPrivateLinkResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2b0d-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b0d-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="e2b0d-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="e2b0d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2b0d-107">DESCRIPTION</span></span>
<span data-ttu-id="e2b0d-108">A **Get-AzPrivateLinkResource** parancsmag lekérdezi az összes forrást, amely a PrivateLinkResource tartozik.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="e2b0d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e2b0d-109">EXAMPLES</span></span>

### <span data-ttu-id="e2b0d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2b0d-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="e2b0d-111">Ebben a példában az összes személyes erőforrás nbelong a mySql nevű SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="e2b0d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2b0d-112">PARAMETERS</span></span>

### <span data-ttu-id="e2b0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b0d-113">-DefaultProfile</span></span>
<span data-ttu-id="e2b0d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b0d-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="e2b0d-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="e2b0d-116">A privát kapcsolat típusú erőforrás Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="e2b0d-116">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b0d-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="e2b0d-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="e2b0d-118">A magánjellegű kapcsolat erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b0d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b0d-119">-ResourceGroupName</span></span>
<span data-ttu-id="e2b0d-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b0d-121">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="e2b0d-121">-ServiceName</span></span>
<span data-ttu-id="e2b0d-122">A privát hivatkozás szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b0d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b0d-123">CommonParameters</span></span>
<span data-ttu-id="e2b0d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2b0d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b0d-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b0d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2b0d-126">INPUTS</span></span>

### <span data-ttu-id="e2b0d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e2b0d-127">System.String</span></span>

## <span data-ttu-id="e2b0d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2b0d-128">OUTPUTS</span></span>

### <span data-ttu-id="e2b0d-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2b0d-129">System.Boolean</span></span>

## <span data-ttu-id="e2b0d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2b0d-130">NOTES</span></span>

## <span data-ttu-id="e2b0d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2b0d-131">RELATED LINKS</span></span>
