---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331961"
---
# <span data-ttu-id="7e163-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="7e163-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="7e163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e163-102">SYNOPSIS</span></span>
<span data-ttu-id="7e163-103">New-AzWebAppContainerPSSession új távoli PowerShell-munkamenetet hoz létre egy adott webhelyen vagy tárolóhelyen és erőforráscsoportban megadott windowsos tárolóban</span><span class="sxs-lookup"><span data-stu-id="7e163-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="7e163-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e163-104">SYNTAX</span></span>

### <span data-ttu-id="7e163-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e163-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e163-106">S2</span><span class="sxs-lookup"><span data-stu-id="7e163-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e163-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e163-107">DESCRIPTION</span></span>
<span data-ttu-id="7e163-108">New-AzWebAppContainerPSSession új távoli PowerShell-munkamenetet hoz létre egy adott webhelyen vagy helyen, illetve erőforráscsoportban megadott windowsos tárolóban</span><span class="sxs-lookup"><span data-stu-id="7e163-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="7e163-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e163-109">EXAMPLES</span></span>

### <span data-ttu-id="7e163-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7e163-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="7e163-111">Ezzel létrehoz egy új távoli PowerShell-munkamenetet a ContosoASP windows-tárolóalkalmazásban, és a ContosoASP tárolón futó folyamatokat mutatja</span><span class="sxs-lookup"><span data-stu-id="7e163-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="7e163-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e163-112">PARAMETERS</span></span>

### <span data-ttu-id="7e163-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e163-113">-DefaultProfile</span></span>
<span data-ttu-id="7e163-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e163-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e163-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7e163-115">-Force</span></span>
<span data-ttu-id="7e163-116">Hozza létre a PowerShell-munkamenetet megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7e163-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7e163-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7e163-117">-Name</span></span>
<span data-ttu-id="7e163-118">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="7e163-118">The name of the web app.</span></span>

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

### <span data-ttu-id="7e163-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e163-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e163-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7e163-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e163-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="7e163-121">-SlotName</span></span>
<span data-ttu-id="7e163-122">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="7e163-122">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e163-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7e163-123">-WebApp</span></span>
<span data-ttu-id="7e163-124">A webalkalmazás-objektum</span><span class="sxs-lookup"><span data-stu-id="7e163-124">The web app object</span></span>

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

### <span data-ttu-id="7e163-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e163-125">-Confirm</span></span>
<span data-ttu-id="7e163-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7e163-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e163-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e163-127">-WhatIf</span></span>
<span data-ttu-id="7e163-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7e163-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e163-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e163-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e163-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e163-130">CommonParameters</span></span>
<span data-ttu-id="7e163-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e163-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e163-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e163-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e163-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e163-133">INPUTS</span></span>

### <span data-ttu-id="7e163-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7e163-134">System.String</span></span>

### <span data-ttu-id="7e163-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7e163-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7e163-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e163-136">OUTPUTS</span></span>

### <span data-ttu-id="7e163-137">System.Management.Automation.Runspaces.PSSession</span><span class="sxs-lookup"><span data-stu-id="7e163-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="7e163-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e163-138">NOTES</span></span>

## <span data-ttu-id="7e163-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e163-139">RELATED LINKS</span></span>
