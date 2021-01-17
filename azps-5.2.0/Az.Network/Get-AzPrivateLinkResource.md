---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364054"
---
# <span data-ttu-id="eda62-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="eda62-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="eda62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda62-102">SYNOPSIS</span></span>
<span data-ttu-id="eda62-103">Privát hivatkozás típusú erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="eda62-103">Gets a private link resource.</span></span>

## <span data-ttu-id="eda62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eda62-104">SYNTAX</span></span>

### <span data-ttu-id="eda62-105">ByPrivateLinkResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eda62-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eda62-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="eda62-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="eda62-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eda62-107">DESCRIPTION</span></span>
<span data-ttu-id="eda62-108">A **Get-AzPrivateLinkResource** parancsmag beolvassa a PrivateLinkResource összes hivatkozási erőforrását.</span><span class="sxs-lookup"><span data-stu-id="eda62-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="eda62-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eda62-109">EXAMPLES</span></span>

### <span data-ttu-id="eda62-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="eda62-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="eda62-111">Az alábbi példa felsorolja az összes privát hivatkozásforrást, amely a mySql nevű sql serverhez van csatolva.</span><span class="sxs-lookup"><span data-stu-id="eda62-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="eda62-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eda62-112">PARAMETERS</span></span>

### <span data-ttu-id="eda62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda62-113">-DefaultProfile</span></span>
<span data-ttu-id="eda62-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eda62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eda62-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="eda62-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="eda62-116">A privát hivatkozás típusú erőforrás Azure-erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eda62-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="eda62-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="eda62-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="eda62-118">A privát csatolás erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="eda62-118">The private link resource type.</span></span>

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

### <span data-ttu-id="eda62-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda62-119">-ResourceGroupName</span></span>
<span data-ttu-id="eda62-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eda62-120">The resource group name.</span></span>

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

### <span data-ttu-id="eda62-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="eda62-121">-ServiceName</span></span>
<span data-ttu-id="eda62-122">A magánjellegű hivatkozásszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="eda62-122">The private link service name.</span></span>

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

### <span data-ttu-id="eda62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda62-123">CommonParameters</span></span>
<span data-ttu-id="eda62-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda62-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eda62-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda62-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eda62-126">INPUTS</span></span>

### <span data-ttu-id="eda62-127">System.String</span><span class="sxs-lookup"><span data-stu-id="eda62-127">System.String</span></span>

## <span data-ttu-id="eda62-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eda62-128">OUTPUTS</span></span>

### <span data-ttu-id="eda62-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eda62-129">System.Boolean</span></span>

## <span data-ttu-id="eda62-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eda62-130">NOTES</span></span>

## <span data-ttu-id="eda62-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eda62-131">RELATED LINKS</span></span>
