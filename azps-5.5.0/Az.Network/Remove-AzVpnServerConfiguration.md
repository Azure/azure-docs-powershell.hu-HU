---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146627"
---
# <span data-ttu-id="67f3d-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="67f3d-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="67f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="67f3d-103">Eltávolít egy meglévő VpnServerConfigurationt.</span><span class="sxs-lookup"><span data-stu-id="67f3d-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="67f3d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="67f3d-104">SYNTAX</span></span>

### <span data-ttu-id="67f3d-105">ByVpnServerConfigurationName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67f3d-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67f3d-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="67f3d-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67f3d-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="67f3d-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67f3d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="67f3d-108">DESCRIPTION</span></span>
<span data-ttu-id="67f3d-109">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="67f3d-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="67f3d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="67f3d-110">EXAMPLES</span></span>

### <span data-ttu-id="67f3d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="67f3d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="67f3d-112">A fenti parancs eltávolít egy meglévő VpnServerConfigurationt.</span><span class="sxs-lookup"><span data-stu-id="67f3d-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="67f3d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67f3d-113">PARAMETERS</span></span>

### <span data-ttu-id="67f3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f3d-114">-DefaultProfile</span></span>
<span data-ttu-id="67f3d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67f3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f3d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="67f3d-116">-Force</span></span>
<span data-ttu-id="67f3d-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67f3d-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="67f3d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67f3d-118">-InputObject</span></span>
<span data-ttu-id="67f3d-119">A vpnServerConfiguration objektumot törölni kell.</span><span class="sxs-lookup"><span data-stu-id="67f3d-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="67f3d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="67f3d-120">-Name</span></span>
<span data-ttu-id="67f3d-121">A vpnServerConfiguration neve.</span><span class="sxs-lookup"><span data-stu-id="67f3d-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="67f3d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67f3d-122">-PassThru</span></span>
<span data-ttu-id="67f3d-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="67f3d-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="67f3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="67f3d-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="67f3d-125">The resource group name.</span></span>

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

### <span data-ttu-id="67f3d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67f3d-126">-ResourceId</span></span>
<span data-ttu-id="67f3d-127">A vpnServerConfiguration Azure-erőforrásazonosítóját törölni kell.</span><span class="sxs-lookup"><span data-stu-id="67f3d-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="67f3d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67f3d-128">-Confirm</span></span>
<span data-ttu-id="67f3d-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="67f3d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67f3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67f3d-130">-WhatIf</span></span>
<span data-ttu-id="67f3d-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="67f3d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67f3d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67f3d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67f3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f3d-133">CommonParameters</span></span>
<span data-ttu-id="67f3d-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f3d-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f3d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f3d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67f3d-136">INPUTS</span></span>

### <span data-ttu-id="67f3d-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="67f3d-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="67f3d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="67f3d-138">System.String</span></span>

## <span data-ttu-id="67f3d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f3d-139">OUTPUTS</span></span>

### <span data-ttu-id="67f3d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67f3d-140">System.Boolean</span></span>

## <span data-ttu-id="67f3d-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="67f3d-141">NOTES</span></span>

## <span data-ttu-id="67f3d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67f3d-142">RELATED LINKS</span></span>
