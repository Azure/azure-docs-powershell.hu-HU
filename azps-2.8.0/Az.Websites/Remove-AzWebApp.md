---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: c91e5ff71a916e28e199a1c64fde2d69f0193fd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840017"
---
# <span data-ttu-id="1d656-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1d656-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="1d656-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d656-102">SYNOPSIS</span></span>
<span data-ttu-id="1d656-103">Azure Web App eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1d656-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="1d656-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d656-104">SYNTAX</span></span>

### <span data-ttu-id="1d656-105">S1</span><span class="sxs-lookup"><span data-stu-id="1d656-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d656-106">S2</span><span class="sxs-lookup"><span data-stu-id="1d656-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d656-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d656-107">DESCRIPTION</span></span>
<span data-ttu-id="1d656-108">A **Remove-AzWebApp** parancsmag eltávolítja az Azure web app alkalmazást, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d656-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="1d656-109">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="1d656-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="1d656-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1d656-110">EXAMPLES</span></span>

### <span data-ttu-id="1d656-111">1. példa: webalkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1d656-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1d656-112">Ez a parancs eltávolítja a ContosoSite nevű Azure webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d656-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1d656-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d656-113">PARAMETERS</span></span>

### <span data-ttu-id="1d656-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d656-114">-AsJob</span></span>
<span data-ttu-id="1d656-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1d656-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d656-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d656-116">-DefaultProfile</span></span>
<span data-ttu-id="1d656-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d656-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d656-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1d656-118">-Force</span></span>
<span data-ttu-id="1d656-119">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="1d656-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="1d656-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d656-120">-Name</span></span>
<span data-ttu-id="1d656-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="1d656-121">WebApp Name</span></span>

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

### <span data-ttu-id="1d656-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d656-122">-ResourceGroupName</span></span>
<span data-ttu-id="1d656-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1d656-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1d656-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1d656-124">-WebApp</span></span>
<span data-ttu-id="1d656-125">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="1d656-125">WebApp Object</span></span>

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

### <span data-ttu-id="1d656-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d656-126">-Confirm</span></span>
<span data-ttu-id="1d656-127">A parancsmag futtatása előtt kéri a megerősítést. A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d656-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d656-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d656-128">-WhatIf</span></span>
<span data-ttu-id="1d656-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d656-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d656-130">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d656-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d656-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d656-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d656-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d656-132">CommonParameters</span></span>
<span data-ttu-id="1d656-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d656-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d656-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d656-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d656-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d656-135">INPUTS</span></span>

### <span data-ttu-id="1d656-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1d656-136">System.String</span></span>

### <span data-ttu-id="1d656-137">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1d656-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1d656-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d656-138">OUTPUTS</span></span>

### <span data-ttu-id="1d656-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="1d656-139">System.Void</span></span>

## <span data-ttu-id="1d656-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d656-140">NOTES</span></span>

## <span data-ttu-id="1d656-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d656-141">RELATED LINKS</span></span>

[<span data-ttu-id="1d656-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1d656-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="1d656-143">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1d656-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="1d656-144">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1d656-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="1d656-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1d656-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="1d656-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1d656-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


