---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b06a5253ac5b26097d2dc4dea9c3d557c00a4d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492659"
---
# <span data-ttu-id="538bc-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="538bc-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="538bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="538bc-102">SYNOPSIS</span></span>
<span data-ttu-id="538bc-103">Azure Web App eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="538bc-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="538bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="538bc-104">SYNTAX</span></span>

### <span data-ttu-id="538bc-105">S1</span><span class="sxs-lookup"><span data-stu-id="538bc-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="538bc-106">S2</span><span class="sxs-lookup"><span data-stu-id="538bc-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="538bc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="538bc-107">DESCRIPTION</span></span>
<span data-ttu-id="538bc-108">A **Remove-AzureRmWebApp** parancsmag eltávolítja az Azure web app alkalmazást, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="538bc-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="538bc-109">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="538bc-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="538bc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="538bc-110">EXAMPLES</span></span>

### <span data-ttu-id="538bc-111">1. példa: webalkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="538bc-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="538bc-112">Ez a parancs eltávolítja a ContosoSite nevű Azure webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="538bc-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="538bc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="538bc-113">PARAMETERS</span></span>

### <span data-ttu-id="538bc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="538bc-114">-AsJob</span></span>
<span data-ttu-id="538bc-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="538bc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="538bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538bc-116">-DefaultProfile</span></span>
<span data-ttu-id="538bc-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="538bc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="538bc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="538bc-118">-Force</span></span>
<span data-ttu-id="538bc-119">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="538bc-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="538bc-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="538bc-120">-Name</span></span>
<span data-ttu-id="538bc-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="538bc-121">WebApp Name</span></span>

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

### <span data-ttu-id="538bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="538bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="538bc-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="538bc-123">Resource Group Name</span></span>

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

### <span data-ttu-id="538bc-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="538bc-124">-WebApp</span></span>
<span data-ttu-id="538bc-125">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="538bc-125">WebApp Object</span></span>

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

### <span data-ttu-id="538bc-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="538bc-126">-Confirm</span></span>
<span data-ttu-id="538bc-127">A parancsmag futtatása előtt kéri a megerősítést. A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="538bc-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="538bc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="538bc-128">-WhatIf</span></span>
<span data-ttu-id="538bc-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="538bc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="538bc-130">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="538bc-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="538bc-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="538bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="538bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538bc-132">CommonParameters</span></span>
<span data-ttu-id="538bc-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="538bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538bc-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="538bc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538bc-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="538bc-135">INPUTS</span></span>

### <span data-ttu-id="538bc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="538bc-136">System.String</span></span>

### <span data-ttu-id="538bc-137">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="538bc-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="538bc-138">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="538bc-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="538bc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="538bc-139">OUTPUTS</span></span>

### <span data-ttu-id="538bc-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="538bc-140">System.Void</span></span>

## <span data-ttu-id="538bc-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="538bc-141">NOTES</span></span>

## <span data-ttu-id="538bc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="538bc-142">RELATED LINKS</span></span>

[<span data-ttu-id="538bc-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="538bc-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="538bc-144">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="538bc-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="538bc-145">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="538bc-145">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="538bc-146">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="538bc-146">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="538bc-147">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="538bc-147">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


