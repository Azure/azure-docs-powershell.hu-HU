---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: e7c0d37dc56e1ff4c986aa66632dccddec283c83
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850214"
---
# <span data-ttu-id="b6517-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6517-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="b6517-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6517-102">SYNOPSIS</span></span>
<span data-ttu-id="b6517-103">Azure Web App eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b6517-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6517-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6517-104">SYNTAX</span></span>

### <span data-ttu-id="b6517-105">S1</span><span class="sxs-lookup"><span data-stu-id="b6517-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6517-106">S2</span><span class="sxs-lookup"><span data-stu-id="b6517-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6517-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6517-107">DESCRIPTION</span></span>
<span data-ttu-id="b6517-108">A **Remove-AzureRmWebApp** parancsmag eltávolítja az Azure web app alkalmazást, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6517-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="b6517-109">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b6517-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="b6517-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b6517-110">EXAMPLES</span></span>

### <span data-ttu-id="b6517-111">1. példa: webalkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6517-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b6517-112">Ez a parancs eltávolítja a ContosoSite nevű Azure webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="b6517-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b6517-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6517-113">PARAMETERS</span></span>

### <span data-ttu-id="b6517-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6517-114">-DefaultProfile</span></span>
<span data-ttu-id="b6517-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6517-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6517-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b6517-116">-Force</span></span>
<span data-ttu-id="b6517-117">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="b6517-117">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6517-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6517-118">-Name</span></span>
<span data-ttu-id="b6517-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="b6517-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6517-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6517-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6517-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b6517-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6517-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b6517-122">-WebApp</span></span>
<span data-ttu-id="b6517-123">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="b6517-123">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6517-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6517-124">-Confirm</span></span>
<span data-ttu-id="b6517-125">A parancsmag futtatása előtt kéri a megerősítést. A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6517-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6517-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6517-126">-WhatIf</span></span>
<span data-ttu-id="b6517-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6517-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6517-128">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6517-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6517-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6517-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6517-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6517-130">-AsJob</span></span>
<span data-ttu-id="b6517-131">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b6517-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6517-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6517-132">CommonParameters</span></span>
<span data-ttu-id="b6517-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6517-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6517-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6517-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6517-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6517-135">INPUTS</span></span>

### <span data-ttu-id="b6517-136">Webhely</span><span class="sxs-lookup"><span data-stu-id="b6517-136">Site</span></span>
<span data-ttu-id="b6517-137">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b6517-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b6517-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6517-138">OUTPUTS</span></span>

## <span data-ttu-id="b6517-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6517-139">NOTES</span></span>

## <span data-ttu-id="b6517-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6517-140">RELATED LINKS</span></span>

[<span data-ttu-id="b6517-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6517-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="b6517-142">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6517-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="b6517-143">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6517-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="b6517-144">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6517-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="b6517-145">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6517-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


