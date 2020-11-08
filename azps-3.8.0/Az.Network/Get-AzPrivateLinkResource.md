---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013303"
---
# <span data-ttu-id="a90b2-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a90b2-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="a90b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a90b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a90b2-103">Személyes hivatkozás típusú erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="a90b2-103">Gets a private link resource.</span></span>

## <span data-ttu-id="a90b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a90b2-104">SYNTAX</span></span>

### <span data-ttu-id="a90b2-105">ByPrivateLinkResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a90b2-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a90b2-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="a90b2-106">DESCRIPTION</span></span>
<span data-ttu-id="a90b2-107">A **Get-AzPrivateLinkResource** parancsmag lekérdezi az összes forrást, amely a PrivateLinkResource tartozik.</span><span class="sxs-lookup"><span data-stu-id="a90b2-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="a90b2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a90b2-108">EXAMPLES</span></span>

### <span data-ttu-id="a90b2-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a90b2-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="a90b2-110">Ebben a példában az összes személyes erőforrás nbelong a mySql nevű SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="a90b2-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="a90b2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a90b2-111">PARAMETERS</span></span>

### <span data-ttu-id="a90b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a90b2-112">-DefaultProfile</span></span>
<span data-ttu-id="a90b2-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a90b2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a90b2-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a90b2-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a90b2-115">A privát kapcsolat típusú erőforrás Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="a90b2-115">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="a90b2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a90b2-116">CommonParameters</span></span>
<span data-ttu-id="a90b2-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a90b2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a90b2-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a90b2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a90b2-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a90b2-119">INPUTS</span></span>

### <span data-ttu-id="a90b2-120">System. String</span><span class="sxs-lookup"><span data-stu-id="a90b2-120">System.String</span></span>

## <span data-ttu-id="a90b2-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a90b2-121">OUTPUTS</span></span>

### <span data-ttu-id="a90b2-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a90b2-122">System.Boolean</span></span>

## <span data-ttu-id="a90b2-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a90b2-123">NOTES</span></span>

## <span data-ttu-id="a90b2-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a90b2-124">RELATED LINKS</span></span>
