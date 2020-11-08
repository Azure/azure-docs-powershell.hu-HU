---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172896"
---
# <span data-ttu-id="1bb89-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="1bb89-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="1bb89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1bb89-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb89-103">Eltávolítja a DNS-zóna csoportját.</span><span class="sxs-lookup"><span data-stu-id="1bb89-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="1bb89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1bb89-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1bb89-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb89-106">A **Remove-AzPrivateDnsZoneGroup** parancsmag eltávolítja a DNS-zóna csoportját.</span><span class="sxs-lookup"><span data-stu-id="1bb89-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="1bb89-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1bb89-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb89-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1bb89-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="1bb89-109">A fenti példa eltávolítja a dnsgroup1 nevű DNS-zóna Grup a végpont-teszt-PR-végpontról.</span><span class="sxs-lookup"><span data-stu-id="1bb89-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="1bb89-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1bb89-110">PARAMETERS</span></span>

### <span data-ttu-id="1bb89-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bb89-111">-AsJob</span></span>
<span data-ttu-id="1bb89-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1bb89-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb89-113">-DefaultProfile</span></span>
<span data-ttu-id="1bb89-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bb89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bb89-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1bb89-115">-Force</span></span>
<span data-ttu-id="1bb89-116">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="1bb89-116">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb89-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1bb89-117">-Name</span></span>
<span data-ttu-id="1bb89-118">A privát DNS-zóna csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1bb89-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb89-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bb89-119">-PassThru</span></span>
<span data-ttu-id="1bb89-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1bb89-120">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb89-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="1bb89-121">-PrivateEndpointName</span></span>
<span data-ttu-id="1bb89-122">A privát végpont neve.</span><span class="sxs-lookup"><span data-stu-id="1bb89-122">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb89-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb89-123">-ResourceGroupName</span></span>
<span data-ttu-id="1bb89-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1bb89-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb89-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1bb89-125">-Confirm</span></span>
<span data-ttu-id="1bb89-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1bb89-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb89-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb89-127">-WhatIf</span></span>
<span data-ttu-id="1bb89-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1bb89-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb89-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1bb89-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb89-130">CommonParameters</span></span>
<span data-ttu-id="1bb89-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1bb89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb89-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1bb89-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb89-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bb89-133">INPUTS</span></span>

### <span data-ttu-id="1bb89-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb89-134">System.String</span></span>

## <span data-ttu-id="1bb89-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bb89-135">OUTPUTS</span></span>

### <span data-ttu-id="1bb89-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bb89-136">System.Boolean</span></span>

## <span data-ttu-id="1bb89-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1bb89-137">NOTES</span></span>

## <span data-ttu-id="1bb89-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bb89-138">RELATED LINKS</span></span>
