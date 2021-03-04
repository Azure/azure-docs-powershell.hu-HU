---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 1ce172ea2f1851f2f75a95a3037798ca3b3a2bf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923146"
---
# <span data-ttu-id="788d1-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="788d1-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="788d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="788d1-102">SYNOPSIS</span></span>
<span data-ttu-id="788d1-103">Eltávolít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="788d1-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="788d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="788d1-104">SYNTAX</span></span>

### <span data-ttu-id="788d1-105">S1</span><span class="sxs-lookup"><span data-stu-id="788d1-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="788d1-106">S2</span><span class="sxs-lookup"><span data-stu-id="788d1-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788d1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="788d1-107">DESCRIPTION</span></span>
<span data-ttu-id="788d1-108">A **Remove-AzWebApp** parancsmag eltávolít egy Azure Web Appot, feltéve hogy az erőforráscsoport és a Web App neve meg van téve.</span><span class="sxs-lookup"><span data-stu-id="788d1-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="788d1-109">Ez a parancsmag alapértelmezés szerint az összes résidőt és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="788d1-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="788d1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="788d1-110">EXAMPLES</span></span>

### <span data-ttu-id="788d1-111">1. példa: Webalkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="788d1-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="788d1-112">Ez a parancs eltávolítja a ContosoSite nevű Azure Web Appot, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="788d1-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="788d1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="788d1-113">PARAMETERS</span></span>

### <span data-ttu-id="788d1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="788d1-114">-AsJob</span></span>
<span data-ttu-id="788d1-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="788d1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="788d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788d1-116">-DefaultProfile</span></span>
<span data-ttu-id="788d1-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="788d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="788d1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="788d1-118">-Force</span></span>
<span data-ttu-id="788d1-119">Forcefully Remove Option</span><span class="sxs-lookup"><span data-stu-id="788d1-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="788d1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="788d1-120">-Name</span></span>
<span data-ttu-id="788d1-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="788d1-121">WebApp Name</span></span>

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

### <span data-ttu-id="788d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="788d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="788d1-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="788d1-123">Resource Group Name</span></span>

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

### <span data-ttu-id="788d1-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="788d1-124">-WebApp</span></span>
<span data-ttu-id="788d1-125">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="788d1-125">WebApp Object</span></span>

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

### <span data-ttu-id="788d1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="788d1-126">-Confirm</span></span>
<span data-ttu-id="788d1-127">A parancsmag futtatása előtt a rendszer megerősítést kér. A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="788d1-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="788d1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788d1-128">-WhatIf</span></span>
<span data-ttu-id="788d1-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="788d1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788d1-130">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="788d1-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788d1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="788d1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="788d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788d1-132">CommonParameters</span></span>
<span data-ttu-id="788d1-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="788d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788d1-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="788d1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788d1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="788d1-135">INPUTS</span></span>

### <span data-ttu-id="788d1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="788d1-136">System.String</span></span>

### <span data-ttu-id="788d1-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="788d1-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="788d1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="788d1-138">OUTPUTS</span></span>

### <span data-ttu-id="788d1-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="788d1-139">System.Void</span></span>

## <span data-ttu-id="788d1-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="788d1-140">NOTES</span></span>

## <span data-ttu-id="788d1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="788d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="788d1-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="788d1-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="788d1-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="788d1-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="788d1-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="788d1-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="788d1-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="788d1-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="788d1-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="788d1-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


