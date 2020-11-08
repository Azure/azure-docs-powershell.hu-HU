---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182982"
---
# <span data-ttu-id="06490-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="06490-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="06490-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06490-102">SYNOPSIS</span></span>
<span data-ttu-id="06490-103">Eltávolítja a meglévő VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="06490-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="06490-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06490-104">SYNTAX</span></span>

### <span data-ttu-id="06490-105">ByVpnServerConfigurationName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06490-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06490-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="06490-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06490-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="06490-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06490-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="06490-108">DESCRIPTION</span></span>
<span data-ttu-id="06490-109">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="06490-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="06490-110">Példák</span><span class="sxs-lookup"><span data-stu-id="06490-110">EXAMPLES</span></span>

### <span data-ttu-id="06490-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06490-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="06490-112">A fenti parancs eltávolítja a meglévő VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="06490-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="06490-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06490-113">PARAMETERS</span></span>

### <span data-ttu-id="06490-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06490-114">-DefaultProfile</span></span>
<span data-ttu-id="06490-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06490-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06490-116">-Force</span><span class="sxs-lookup"><span data-stu-id="06490-116">-Force</span></span>
<span data-ttu-id="06490-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06490-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="06490-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06490-118">-InputObject</span></span>
<span data-ttu-id="06490-119">A törlendő vpnServerConfiguration objektum.</span><span class="sxs-lookup"><span data-stu-id="06490-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06490-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06490-120">-Name</span></span>
<span data-ttu-id="06490-121">A vpnServerConfiguration neve.</span><span class="sxs-lookup"><span data-stu-id="06490-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06490-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06490-122">-PassThru</span></span>
<span data-ttu-id="06490-123">Egy olyan objektumot ad eredményül, amely azt az elemet jeleníti meg, amelyen a művelet végre van hajtva.</span><span class="sxs-lookup"><span data-stu-id="06490-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="06490-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06490-124">-ResourceGroupName</span></span>
<span data-ttu-id="06490-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="06490-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06490-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06490-126">-ResourceId</span></span>
<span data-ttu-id="06490-127">A törlendő vpnServerConfiguration Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="06490-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06490-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06490-128">-Confirm</span></span>
<span data-ttu-id="06490-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06490-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06490-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06490-130">-WhatIf</span></span>
<span data-ttu-id="06490-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06490-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06490-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06490-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06490-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06490-133">CommonParameters</span></span>
<span data-ttu-id="06490-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06490-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06490-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06490-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06490-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06490-136">INPUTS</span></span>

### <span data-ttu-id="06490-137">Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="06490-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="06490-138">System. String</span><span class="sxs-lookup"><span data-stu-id="06490-138">System.String</span></span>

## <span data-ttu-id="06490-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06490-139">OUTPUTS</span></span>

### <span data-ttu-id="06490-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06490-140">System.Boolean</span></span>

## <span data-ttu-id="06490-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06490-141">NOTES</span></span>

## <span data-ttu-id="06490-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06490-142">RELATED LINKS</span></span>
