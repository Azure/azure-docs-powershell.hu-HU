---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172897"
---
# <span data-ttu-id="6c08b-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c08b-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6c08b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c08b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c08b-103">Eltávolítja a meglévő P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6c08b-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="6c08b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c08b-104">SYNTAX</span></span>

### <span data-ttu-id="6c08b-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6c08b-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c08b-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6c08b-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c08b-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6c08b-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c08b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c08b-108">DESCRIPTION</span></span>
<span data-ttu-id="6c08b-109">A **Remove-AzP2sVpnGateway** parancsmag lehetővé teszi a meglévő P2SVpnGateway eltávolítását a VirtualHub csoportban.</span><span class="sxs-lookup"><span data-stu-id="6c08b-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="6c08b-110">A P2SVpnGateway eltávolítása után a webhely ügyfeleinek kapcsolódási pontja sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="6c08b-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="6c08b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6c08b-111">EXAMPLES</span></span>

### <span data-ttu-id="6c08b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6c08b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="6c08b-113">A **Remove-AzP2sVpnGateway** parancsmag lehetővé teszi a meglévő P2SVpnGateway eltávolítását a VirtualHub csoportban.</span><span class="sxs-lookup"><span data-stu-id="6c08b-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="6c08b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c08b-114">PARAMETERS</span></span>

### <span data-ttu-id="6c08b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c08b-115">-DefaultProfile</span></span>
<span data-ttu-id="6c08b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c08b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c08b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6c08b-117">-Force</span></span>
<span data-ttu-id="6c08b-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c08b-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6c08b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c08b-119">-InputObject</span></span>
<span data-ttu-id="6c08b-120">A törlendő p2sVpnGateway objektum.</span><span class="sxs-lookup"><span data-stu-id="6c08b-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="6c08b-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c08b-121">-Name</span></span>
<span data-ttu-id="6c08b-122">A P2SVpnGateway neve.</span><span class="sxs-lookup"><span data-stu-id="6c08b-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="6c08b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c08b-123">-PassThru</span></span>
<span data-ttu-id="6c08b-124">Egy olyan objektumot ad eredményül, amely azt az elemet jeleníti meg, amelyen a művelet végre van hajtva.</span><span class="sxs-lookup"><span data-stu-id="6c08b-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="6c08b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c08b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c08b-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c08b-126">The resource group name.</span></span>

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

### <span data-ttu-id="6c08b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c08b-127">-ResourceId</span></span>
<span data-ttu-id="6c08b-128">A törlendő p2sVpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="6c08b-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="6c08b-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c08b-129">-Confirm</span></span>
<span data-ttu-id="6c08b-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c08b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c08b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c08b-131">-WhatIf</span></span>
<span data-ttu-id="6c08b-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c08b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c08b-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c08b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c08b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c08b-134">CommonParameters</span></span>
<span data-ttu-id="6c08b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c08b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c08b-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c08b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c08b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c08b-137">INPUTS</span></span>

### <span data-ttu-id="6c08b-138">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c08b-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="6c08b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6c08b-139">System.String</span></span>

## <span data-ttu-id="6c08b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c08b-140">OUTPUTS</span></span>

### <span data-ttu-id="6c08b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c08b-141">System.Boolean</span></span>

## <span data-ttu-id="6c08b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c08b-142">NOTES</span></span>

## <span data-ttu-id="6c08b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c08b-143">RELATED LINKS</span></span>
