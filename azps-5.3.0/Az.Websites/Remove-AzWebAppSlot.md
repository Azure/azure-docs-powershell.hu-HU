---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466983"
---
# <span data-ttu-id="86b70-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86b70-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="86b70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86b70-102">SYNOPSIS</span></span>

## <span data-ttu-id="86b70-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86b70-103">SYNTAX</span></span>

### <span data-ttu-id="86b70-104">S1</span><span class="sxs-lookup"><span data-stu-id="86b70-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86b70-105">S2</span><span class="sxs-lookup"><span data-stu-id="86b70-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86b70-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86b70-106">DESCRIPTION</span></span>
<span data-ttu-id="86b70-107">A **Remove-AzWebAppSzaj** parancsmag eltávolítja az Azure Web App Slotot, feltéve hogy az erőforráscsoport és a Web App neve meg van téve.</span><span class="sxs-lookup"><span data-stu-id="86b70-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="86b70-108">Ez a parancsmag alapértelmezés szerint az összes résidőt és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="86b70-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="86b70-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86b70-109">EXAMPLES</span></span>

### <span data-ttu-id="86b70-110">1. példa: Web apphely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="86b70-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="86b70-111">Ez a parancs eltávolítja a Slot001 nevű slotot, amely a ContosoSite webalkalmazáshoz van társítva, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="86b70-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="86b70-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86b70-112">PARAMETERS</span></span>

### <span data-ttu-id="86b70-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86b70-113">-AsJob</span></span>
<span data-ttu-id="86b70-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="86b70-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86b70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b70-115">-DefaultProfile</span></span>
<span data-ttu-id="86b70-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86b70-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86b70-117">-Force</span><span class="sxs-lookup"><span data-stu-id="86b70-117">-Force</span></span>
<span data-ttu-id="86b70-118">Forcefully Remove Option</span><span class="sxs-lookup"><span data-stu-id="86b70-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="86b70-119">-Name</span><span class="sxs-lookup"><span data-stu-id="86b70-119">-Name</span></span>
<span data-ttu-id="86b70-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="86b70-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b70-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86b70-121">-ResourceGroupName</span></span>
<span data-ttu-id="86b70-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="86b70-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b70-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="86b70-123">-Slot</span></span>
<span data-ttu-id="86b70-124">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="86b70-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b70-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="86b70-125">-WebApp</span></span>
<span data-ttu-id="86b70-126">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="86b70-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86b70-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86b70-127">-Confirm</span></span>
<span data-ttu-id="86b70-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="86b70-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86b70-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86b70-129">-WhatIf</span></span>
<span data-ttu-id="86b70-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="86b70-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86b70-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86b70-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86b70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b70-132">CommonParameters</span></span>
<span data-ttu-id="86b70-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86b70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b70-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86b70-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b70-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86b70-135">INPUTS</span></span>

### <span data-ttu-id="86b70-136">System.String</span><span class="sxs-lookup"><span data-stu-id="86b70-136">System.String</span></span>

### <span data-ttu-id="86b70-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="86b70-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="86b70-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86b70-138">OUTPUTS</span></span>

### <span data-ttu-id="86b70-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="86b70-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="86b70-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86b70-140">NOTES</span></span>

## <span data-ttu-id="86b70-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86b70-141">RELATED LINKS</span></span>

[<span data-ttu-id="86b70-142">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="86b70-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="86b70-143">New-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="86b70-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="86b70-144">Restart-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="86b70-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="86b70-145">Set-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="86b70-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="86b70-146">Start-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="86b70-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="86b70-147">Stop-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="86b70-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="86b70-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86b70-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
