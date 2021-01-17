---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481211"
---
# <span data-ttu-id="3b79b-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3b79b-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="3b79b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b79b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b79b-103">Eltávolít egy meglévő P2SVpnGatewayt.</span><span class="sxs-lookup"><span data-stu-id="3b79b-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="3b79b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3b79b-104">SYNTAX</span></span>

### <span data-ttu-id="3b79b-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b79b-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b79b-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="3b79b-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b79b-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3b79b-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b79b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3b79b-108">DESCRIPTION</span></span>
<span data-ttu-id="3b79b-109">A **Remove-AzP2sVpnGateway** parancsmag lehetővé teszi egy meglévő P2SVpnGateway eltávolítását a VirtualHub alatt.</span><span class="sxs-lookup"><span data-stu-id="3b79b-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="3b79b-110">A P2SVpnGateway eltávolítása után a webhely ügyfeleinek csatlakozási pontja meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="3b79b-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="3b79b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3b79b-111">EXAMPLES</span></span>

### <span data-ttu-id="3b79b-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3b79b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="3b79b-113">A **Remove-AzP2sVpnGateway** parancsmag lehetővé teszi egy meglévő P2SVpnGateway eltávolítását a VirtualHub alatt.</span><span class="sxs-lookup"><span data-stu-id="3b79b-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="3b79b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b79b-114">PARAMETERS</span></span>

### <span data-ttu-id="3b79b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b79b-115">-DefaultProfile</span></span>
<span data-ttu-id="3b79b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b79b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3b79b-117">-Force</span></span>
<span data-ttu-id="3b79b-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b79b-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b79b-119">-InputObject</span></span>
<span data-ttu-id="3b79b-120">A törölni szükséges p2sVpnGateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="3b79b-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3b79b-121">-Name</span></span>
<span data-ttu-id="3b79b-122">A P2SVpnGateway neve.</span><span class="sxs-lookup"><span data-stu-id="3b79b-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b79b-123">-PassThru</span></span>
<span data-ttu-id="3b79b-124">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="3b79b-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b79b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3b79b-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3b79b-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b79b-127">-ResourceId</span></span>
<span data-ttu-id="3b79b-128">A törölnie kell a p2sVpnGateway Azure-erőforrásazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="3b79b-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b79b-129">-Confirm</span></span>
<span data-ttu-id="3b79b-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3b79b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b79b-131">-WhatIf</span></span>
<span data-ttu-id="3b79b-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3b79b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b79b-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b79b-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b79b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b79b-134">CommonParameters</span></span>
<span data-ttu-id="3b79b-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b79b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b79b-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b79b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b79b-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b79b-137">INPUTS</span></span>

### <span data-ttu-id="3b79b-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3b79b-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="3b79b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3b79b-139">System.String</span></span>

## <span data-ttu-id="3b79b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b79b-140">OUTPUTS</span></span>

### <span data-ttu-id="3b79b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b79b-141">System.Boolean</span></span>

## <span data-ttu-id="3b79b-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3b79b-142">NOTES</span></span>

## <span data-ttu-id="3b79b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b79b-143">RELATED LINKS</span></span>
