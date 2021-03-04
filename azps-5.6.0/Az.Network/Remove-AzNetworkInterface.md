---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 54bc4a3b9875f68df8a7c824c7e4f754e6f35a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940105"
---
# <span data-ttu-id="70007-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="70007-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="70007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70007-102">SYNOPSIS</span></span>
<span data-ttu-id="70007-103">Eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="70007-103">Removes a network interface.</span></span>

## <span data-ttu-id="70007-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70007-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70007-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70007-105">DESCRIPTION</span></span>
<span data-ttu-id="70007-106">A **Remove-AzNetworkInterface** parancsmag eltávolítja az Azure hálózati felületét.</span><span class="sxs-lookup"><span data-stu-id="70007-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="70007-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70007-107">EXAMPLES</span></span>

### <span data-ttu-id="70007-108">1. példa: Hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70007-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="70007-109">Ez a parancs eltávolítja a NetworkInterface1 hálózati felületet az ResourceGroup1 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="70007-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="70007-110">Mivel a *Force* paramétert nem használja, a rendszer kérni fogja a felhasználótól a művelet megerősítését.</span><span class="sxs-lookup"><span data-stu-id="70007-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="70007-111">2. példa: Hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70007-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="70007-112">Ez a parancs eltávolítja az Erőforráscsoport1 erőforráscsoport összes hálózati felületét.</span><span class="sxs-lookup"><span data-stu-id="70007-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="70007-113">Mivel a *Force* paramétert használja, a felhasználó nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70007-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="70007-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70007-114">PARAMETERS</span></span>

### <span data-ttu-id="70007-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70007-115">-AsJob</span></span>
<span data-ttu-id="70007-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="70007-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70007-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70007-117">-DefaultProfile</span></span>
<span data-ttu-id="70007-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70007-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70007-119">-Force</span><span class="sxs-lookup"><span data-stu-id="70007-119">-Force</span></span>
<span data-ttu-id="70007-120">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="70007-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="70007-121">-Name</span><span class="sxs-lookup"><span data-stu-id="70007-121">-Name</span></span>
<span data-ttu-id="70007-122">Annak a hálózati felületnek a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70007-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70007-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70007-123">-PassThru</span></span>
<span data-ttu-id="70007-124">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="70007-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="70007-125">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="70007-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70007-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70007-126">-ResourceGroupName</span></span>
<span data-ttu-id="70007-127">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által eltávolított hálózati felületet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="70007-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="70007-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70007-128">-Confirm</span></span>
<span data-ttu-id="70007-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="70007-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70007-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70007-130">-WhatIf</span></span>
<span data-ttu-id="70007-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="70007-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70007-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70007-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70007-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70007-133">CommonParameters</span></span>
<span data-ttu-id="70007-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70007-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70007-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70007-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70007-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70007-136">INPUTS</span></span>

### <span data-ttu-id="70007-137">System.String</span><span class="sxs-lookup"><span data-stu-id="70007-137">System.String</span></span>

## <span data-ttu-id="70007-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70007-138">OUTPUTS</span></span>

### <span data-ttu-id="70007-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70007-139">System.Boolean</span></span>

## <span data-ttu-id="70007-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70007-140">NOTES</span></span>

## <span data-ttu-id="70007-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70007-141">RELATED LINKS</span></span>

[<span data-ttu-id="70007-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="70007-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="70007-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="70007-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="70007-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="70007-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


