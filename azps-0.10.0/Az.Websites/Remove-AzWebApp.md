---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 40b14128ec2a1dc48cf098a2c0427728c34c7e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842726"
---
# <span data-ttu-id="3e44c-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e44c-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="3e44c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e44c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e44c-103">Azure Web App eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3e44c-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="3e44c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e44c-104">SYNTAX</span></span>

### <span data-ttu-id="3e44c-105">S1</span><span class="sxs-lookup"><span data-stu-id="3e44c-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e44c-106">S2</span><span class="sxs-lookup"><span data-stu-id="3e44c-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e44c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e44c-107">DESCRIPTION</span></span>
<span data-ttu-id="3e44c-108">A **Remove-AzWebApp** parancsmag eltávolítja az Azure web app alkalmazást, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e44c-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="3e44c-109">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="3e44c-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="3e44c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3e44c-110">EXAMPLES</span></span>

### <span data-ttu-id="3e44c-111">1. példa: webalkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3e44c-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3e44c-112">Ez a parancs eltávolítja a ContosoSite nevű Azure webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="3e44c-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3e44c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e44c-113">PARAMETERS</span></span>

### <span data-ttu-id="3e44c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e44c-114">-DefaultProfile</span></span>
<span data-ttu-id="3e44c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e44c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e44c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3e44c-116">-Force</span></span>
<span data-ttu-id="3e44c-117">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="3e44c-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="3e44c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e44c-118">-Name</span></span>
<span data-ttu-id="3e44c-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="3e44c-119">WebApp Name</span></span>

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

### <span data-ttu-id="3e44c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e44c-120">-ResourceGroupName</span></span>
<span data-ttu-id="3e44c-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3e44c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="3e44c-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3e44c-122">-WebApp</span></span>
<span data-ttu-id="3e44c-123">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="3e44c-123">WebApp Object</span></span>

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

### <span data-ttu-id="3e44c-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e44c-124">-Confirm</span></span>
<span data-ttu-id="3e44c-125">A parancsmag futtatása előtt kéri a megerősítést. A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e44c-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e44c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e44c-126">-WhatIf</span></span>
<span data-ttu-id="3e44c-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e44c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e44c-128">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e44c-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e44c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e44c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e44c-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e44c-130">-AsJob</span></span>
<span data-ttu-id="3e44c-131">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3e44c-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e44c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e44c-132">CommonParameters</span></span>
<span data-ttu-id="3e44c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e44c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e44c-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e44c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e44c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e44c-135">INPUTS</span></span>

### <span data-ttu-id="3e44c-136">Webhely</span><span class="sxs-lookup"><span data-stu-id="3e44c-136">Site</span></span>
<span data-ttu-id="3e44c-137">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3e44c-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3e44c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e44c-138">OUTPUTS</span></span>

## <span data-ttu-id="3e44c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e44c-139">NOTES</span></span>

## <span data-ttu-id="3e44c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e44c-140">RELATED LINKS</span></span>

[<span data-ttu-id="3e44c-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e44c-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3e44c-142">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e44c-142">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3e44c-143">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e44c-143">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3e44c-144">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e44c-144">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="3e44c-145">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e44c-145">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


