---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025022"
---
# <span data-ttu-id="b4740-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4740-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="b4740-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4740-102">SYNOPSIS</span></span>
<span data-ttu-id="b4740-103">Azure Web App eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b4740-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="b4740-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4740-104">SYNTAX</span></span>

### <span data-ttu-id="b4740-105">S1</span><span class="sxs-lookup"><span data-stu-id="b4740-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4740-106">S2</span><span class="sxs-lookup"><span data-stu-id="b4740-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4740-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4740-107">DESCRIPTION</span></span>
<span data-ttu-id="b4740-108">A **Remove-AzWebApp** parancsmag eltávolítja az Azure web app alkalmazást, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4740-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="b4740-109">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b4740-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="b4740-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b4740-110">EXAMPLES</span></span>

### <span data-ttu-id="b4740-111">1. példa: webalkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b4740-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b4740-112">Ez a parancs eltávolítja a ContosoSite nevű Azure webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="b4740-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b4740-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4740-113">PARAMETERS</span></span>

### <span data-ttu-id="b4740-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4740-114">-AsJob</span></span>
<span data-ttu-id="b4740-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b4740-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4740-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4740-116">-DefaultProfile</span></span>
<span data-ttu-id="b4740-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4740-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4740-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b4740-118">-Force</span></span>
<span data-ttu-id="b4740-119">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="b4740-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="b4740-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4740-120">-Name</span></span>
<span data-ttu-id="b4740-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="b4740-121">WebApp Name</span></span>

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

### <span data-ttu-id="b4740-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4740-122">-ResourceGroupName</span></span>
<span data-ttu-id="b4740-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b4740-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b4740-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b4740-124">-WebApp</span></span>
<span data-ttu-id="b4740-125">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="b4740-125">WebApp Object</span></span>

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

### <span data-ttu-id="b4740-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4740-126">-Confirm</span></span>
<span data-ttu-id="b4740-127">A parancsmag futtatása előtt kéri a megerősítést. A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4740-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4740-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4740-128">-WhatIf</span></span>
<span data-ttu-id="b4740-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4740-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4740-130">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4740-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4740-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4740-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4740-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4740-132">CommonParameters</span></span>
<span data-ttu-id="b4740-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4740-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4740-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4740-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4740-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4740-135">INPUTS</span></span>

### <span data-ttu-id="b4740-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b4740-136">System.String</span></span>

### <span data-ttu-id="b4740-137">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b4740-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b4740-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4740-138">OUTPUTS</span></span>

### <span data-ttu-id="b4740-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="b4740-139">System.Void</span></span>

## <span data-ttu-id="b4740-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4740-140">NOTES</span></span>

## <span data-ttu-id="b4740-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4740-141">RELATED LINKS</span></span>

[<span data-ttu-id="b4740-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4740-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b4740-143">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4740-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b4740-144">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4740-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b4740-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4740-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b4740-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4740-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


