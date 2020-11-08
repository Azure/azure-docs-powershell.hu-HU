---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010727"
---
# <span data-ttu-id="60eb7-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60eb7-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="60eb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="60eb7-103">Azure Web App eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="60eb7-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="60eb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60eb7-104">SYNTAX</span></span>

### <span data-ttu-id="60eb7-105">S1</span><span class="sxs-lookup"><span data-stu-id="60eb7-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60eb7-106">S2</span><span class="sxs-lookup"><span data-stu-id="60eb7-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60eb7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="60eb7-107">DESCRIPTION</span></span>
<span data-ttu-id="60eb7-108">A **Remove-AzWebApp** parancsmag eltávolítja az Azure web app alkalmazást, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60eb7-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="60eb7-109">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="60eb7-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="60eb7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="60eb7-110">EXAMPLES</span></span>

### <span data-ttu-id="60eb7-111">1. példa: webalkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="60eb7-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="60eb7-112">Ez a parancs eltávolítja a ContosoSite nevű Azure webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="60eb7-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="60eb7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60eb7-113">PARAMETERS</span></span>

### <span data-ttu-id="60eb7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60eb7-114">-AsJob</span></span>
<span data-ttu-id="60eb7-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="60eb7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60eb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60eb7-116">-DefaultProfile</span></span>
<span data-ttu-id="60eb7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60eb7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60eb7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="60eb7-118">-Force</span></span>
<span data-ttu-id="60eb7-119">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="60eb7-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="60eb7-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60eb7-120">-Name</span></span>
<span data-ttu-id="60eb7-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="60eb7-121">WebApp Name</span></span>

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

### <span data-ttu-id="60eb7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60eb7-122">-ResourceGroupName</span></span>
<span data-ttu-id="60eb7-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="60eb7-123">Resource Group Name</span></span>

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

### <span data-ttu-id="60eb7-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="60eb7-124">-WebApp</span></span>
<span data-ttu-id="60eb7-125">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="60eb7-125">WebApp Object</span></span>

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

### <span data-ttu-id="60eb7-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60eb7-126">-Confirm</span></span>
<span data-ttu-id="60eb7-127">A parancsmag futtatása előtt kéri a megerősítést. A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60eb7-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60eb7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60eb7-128">-WhatIf</span></span>
<span data-ttu-id="60eb7-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60eb7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60eb7-130">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60eb7-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60eb7-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60eb7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60eb7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60eb7-132">CommonParameters</span></span>
<span data-ttu-id="60eb7-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60eb7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60eb7-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60eb7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60eb7-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60eb7-135">INPUTS</span></span>

### <span data-ttu-id="60eb7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60eb7-136">System.String</span></span>

### <span data-ttu-id="60eb7-137">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="60eb7-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="60eb7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60eb7-138">OUTPUTS</span></span>

### <span data-ttu-id="60eb7-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="60eb7-139">System.Void</span></span>

## <span data-ttu-id="60eb7-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60eb7-140">NOTES</span></span>

## <span data-ttu-id="60eb7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60eb7-141">RELATED LINKS</span></span>

[<span data-ttu-id="60eb7-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60eb7-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="60eb7-143">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60eb7-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="60eb7-144">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60eb7-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="60eb7-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60eb7-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="60eb7-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60eb7-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


