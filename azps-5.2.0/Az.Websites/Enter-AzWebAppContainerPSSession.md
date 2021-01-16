---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347333"
---
# <span data-ttu-id="cc023-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="cc023-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="cc023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc023-102">SYNOPSIS</span></span>
<span data-ttu-id="cc023-103">Távoli PowerShell-munkamenet megnyitása egy adott webhelyen vagy tárolóhelyen és erőforráscsoportban megadott windows-tárolóban</span><span class="sxs-lookup"><span data-stu-id="cc023-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="cc023-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc023-104">SYNTAX</span></span>

### <span data-ttu-id="cc023-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc023-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc023-106">S2</span><span class="sxs-lookup"><span data-stu-id="cc023-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc023-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc023-107">DESCRIPTION</span></span>
<span data-ttu-id="cc023-108">távoli PowerShell-munkamenet megnyitása egy adott webhelyen vagy tárolóhelyen és erőforráscsoportban megadott windows-tárolóban</span><span class="sxs-lookup"><span data-stu-id="cc023-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="cc023-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc023-109">EXAMPLES</span></span>

### <span data-ttu-id="cc023-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cc023-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="cc023-111">Ez a parancs megnyit egy távoli PowerShell-munkamenetet a ContosoASP windows-tárolóalkalmazásban</span><span class="sxs-lookup"><span data-stu-id="cc023-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="cc023-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc023-112">PARAMETERS</span></span>

### <span data-ttu-id="cc023-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc023-113">-DefaultProfile</span></span>
<span data-ttu-id="cc023-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc023-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc023-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc023-115">-Force</span></span>
<span data-ttu-id="cc023-116">Hozza létre a PowerShell-munkamenetet megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cc023-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cc023-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cc023-117">-Name</span></span>
<span data-ttu-id="cc023-118">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="cc023-118">The name of the web app.</span></span>

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

### <span data-ttu-id="cc023-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc023-119">-PassThru</span></span>
<span data-ttu-id="cc023-120">Sikeres vagy sikertelenséget jelző értéket ad vissza</span><span class="sxs-lookup"><span data-stu-id="cc023-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="cc023-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc023-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc023-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cc023-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc023-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="cc023-123">-SlotName</span></span>
<span data-ttu-id="cc023-124">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="cc023-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="cc023-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cc023-125">-WebApp</span></span>
<span data-ttu-id="cc023-126">A webalkalmazás-objektum</span><span class="sxs-lookup"><span data-stu-id="cc023-126">The web app object</span></span>

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

### <span data-ttu-id="cc023-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc023-127">-Confirm</span></span>
<span data-ttu-id="cc023-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cc023-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc023-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc023-129">-WhatIf</span></span>
<span data-ttu-id="cc023-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cc023-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc023-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc023-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc023-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc023-132">CommonParameters</span></span>
<span data-ttu-id="cc023-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc023-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc023-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc023-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc023-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc023-135">INPUTS</span></span>

### <span data-ttu-id="cc023-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cc023-136">System.String</span></span>

### <span data-ttu-id="cc023-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="cc023-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cc023-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc023-138">OUTPUTS</span></span>

### <span data-ttu-id="cc023-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="cc023-139">System.Void</span></span>

## <span data-ttu-id="cc023-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc023-140">NOTES</span></span>

## <span data-ttu-id="cc023-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc023-141">RELATED LINKS</span></span>
