---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149675"
---
# <span data-ttu-id="57261-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57261-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="57261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57261-102">SYNOPSIS</span></span>
<span data-ttu-id="57261-103">Eltávolít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="57261-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="57261-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57261-104">SYNTAX</span></span>

### <span data-ttu-id="57261-105">S1</span><span class="sxs-lookup"><span data-stu-id="57261-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57261-106">S2</span><span class="sxs-lookup"><span data-stu-id="57261-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57261-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57261-107">DESCRIPTION</span></span>
<span data-ttu-id="57261-108">A **Remove-AzWebApp** parancsmag eltávolít egy Azure Web Appot, feltéve hogy az erőforráscsoport és a Web App neve meg van téve.</span><span class="sxs-lookup"><span data-stu-id="57261-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="57261-109">Ez a parancsmag alapértelmezés szerint az összes résidőt és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="57261-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="57261-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57261-110">EXAMPLES</span></span>

### <span data-ttu-id="57261-111">1. példa: Webalkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="57261-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="57261-112">Ez a parancs eltávolítja a ContosoSite nevű Azure Web Appot, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="57261-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="57261-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57261-113">PARAMETERS</span></span>

### <span data-ttu-id="57261-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57261-114">-AsJob</span></span>
<span data-ttu-id="57261-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="57261-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57261-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57261-116">-DefaultProfile</span></span>
<span data-ttu-id="57261-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57261-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57261-118">-Force</span><span class="sxs-lookup"><span data-stu-id="57261-118">-Force</span></span>
<span data-ttu-id="57261-119">Forcefully Remove Option</span><span class="sxs-lookup"><span data-stu-id="57261-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="57261-120">-Name</span><span class="sxs-lookup"><span data-stu-id="57261-120">-Name</span></span>
<span data-ttu-id="57261-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="57261-121">WebApp Name</span></span>

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

### <span data-ttu-id="57261-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57261-122">-ResourceGroupName</span></span>
<span data-ttu-id="57261-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="57261-123">Resource Group Name</span></span>

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

### <span data-ttu-id="57261-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="57261-124">-WebApp</span></span>
<span data-ttu-id="57261-125">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="57261-125">WebApp Object</span></span>

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

### <span data-ttu-id="57261-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57261-126">-Confirm</span></span>
<span data-ttu-id="57261-127">A parancsmag futtatása előtt a rendszer megerősítést kér. A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="57261-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57261-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57261-128">-WhatIf</span></span>
<span data-ttu-id="57261-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="57261-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57261-130">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="57261-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57261-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57261-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57261-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57261-132">CommonParameters</span></span>
<span data-ttu-id="57261-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57261-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57261-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57261-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57261-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57261-135">INPUTS</span></span>

### <span data-ttu-id="57261-136">System.String</span><span class="sxs-lookup"><span data-stu-id="57261-136">System.String</span></span>

### <span data-ttu-id="57261-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="57261-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="57261-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57261-138">OUTPUTS</span></span>

### <span data-ttu-id="57261-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="57261-139">System.Void</span></span>

## <span data-ttu-id="57261-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57261-140">NOTES</span></span>

## <span data-ttu-id="57261-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57261-141">RELATED LINKS</span></span>

[<span data-ttu-id="57261-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57261-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="57261-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57261-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="57261-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57261-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="57261-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57261-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="57261-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57261-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


