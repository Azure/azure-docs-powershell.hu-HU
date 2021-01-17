---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468938"
---
# <span data-ttu-id="dd2d9-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dd2d9-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="dd2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2d9-103">Tűzfal eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd2d9-103">Remove a Firewall.</span></span>

## <span data-ttu-id="dd2d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd2d9-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd2d9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd2d9-105">DESCRIPTION</span></span>
<span data-ttu-id="dd2d9-106">A **Remove-AzFirewall** parancsmag eltávolítja az Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="dd2d9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd2d9-107">EXAMPLES</span></span>

### <span data-ttu-id="dd2d9-108">1. példa: Tűzfal létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="dd2d9-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="dd2d9-109">Ez a példa létrehoz egy tűzfalat, majd törli azt.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="dd2d9-110">A tűzfal törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="dd2d9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd2d9-111">PARAMETERS</span></span>

### <span data-ttu-id="dd2d9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd2d9-112">-AsJob</span></span>
<span data-ttu-id="dd2d9-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dd2d9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd2d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2d9-114">-DefaultProfile</span></span>
<span data-ttu-id="dd2d9-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd2d9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dd2d9-116">-Force</span></span>
<span data-ttu-id="dd2d9-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dd2d9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="dd2d9-118">-Name</span></span>
<span data-ttu-id="dd2d9-119">Annak a tűzfalnak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd2d9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd2d9-120">-PassThru</span></span>
<span data-ttu-id="dd2d9-121">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd2d9-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd2d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd2d9-124">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által eltávolított tűzfalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd2d9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd2d9-125">-Confirm</span></span>
<span data-ttu-id="dd2d9-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd2d9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2d9-127">-WhatIf</span></span>
<span data-ttu-id="dd2d9-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2d9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd2d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2d9-130">CommonParameters</span></span>
<span data-ttu-id="dd2d9-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2d9-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2d9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2d9-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd2d9-133">INPUTS</span></span>

### <span data-ttu-id="dd2d9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dd2d9-134">System.String</span></span>

## <span data-ttu-id="dd2d9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd2d9-135">OUTPUTS</span></span>

### <span data-ttu-id="dd2d9-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd2d9-136">System.Boolean</span></span>

## <span data-ttu-id="dd2d9-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd2d9-137">NOTES</span></span>

## <span data-ttu-id="dd2d9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd2d9-138">RELATED LINKS</span></span>

[<span data-ttu-id="dd2d9-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dd2d9-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="dd2d9-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dd2d9-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="dd2d9-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dd2d9-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
