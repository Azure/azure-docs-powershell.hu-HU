---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180553"
---
# <span data-ttu-id="8a100-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8a100-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="8a100-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a100-102">SYNOPSIS</span></span>
<span data-ttu-id="8a100-103">Személyes hivatkozás típusú erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="8a100-103">Gets a private link resource.</span></span>

## <span data-ttu-id="8a100-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a100-104">SYNTAX</span></span>

### <span data-ttu-id="8a100-105">ByPrivateLinkResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a100-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a100-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a100-106">DESCRIPTION</span></span>
<span data-ttu-id="8a100-107">A **Get-AzPrivateLinkResource** parancsmag lekérdezi az összes forrást, amely a PrivateLinkResource tartozik.</span><span class="sxs-lookup"><span data-stu-id="8a100-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="8a100-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8a100-108">EXAMPLES</span></span>

### <span data-ttu-id="8a100-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8a100-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="8a100-110">Ebben a példában az összes személyes erőforrás nbelong a mySql nevű SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="8a100-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="8a100-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a100-111">PARAMETERS</span></span>

### <span data-ttu-id="8a100-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a100-112">-DefaultProfile</span></span>
<span data-ttu-id="8a100-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a100-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a100-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="8a100-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="8a100-115">A privát kapcsolat típusú erőforrás Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="8a100-115">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="8a100-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a100-116">CommonParameters</span></span>
<span data-ttu-id="8a100-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a100-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a100-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8a100-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a100-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a100-119">INPUTS</span></span>

### <span data-ttu-id="8a100-120">System. String</span><span class="sxs-lookup"><span data-stu-id="8a100-120">System.String</span></span>

## <span data-ttu-id="8a100-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a100-121">OUTPUTS</span></span>

### <span data-ttu-id="8a100-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a100-122">System.Boolean</span></span>

## <span data-ttu-id="8a100-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a100-123">NOTES</span></span>

## <span data-ttu-id="8a100-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a100-124">RELATED LINKS</span></span>
