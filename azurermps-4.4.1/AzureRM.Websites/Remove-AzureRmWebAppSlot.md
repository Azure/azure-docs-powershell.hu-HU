---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504659"
---
# <span data-ttu-id="fadd4-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fadd4-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="fadd4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fadd4-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fadd4-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fadd4-103">SYNTAX</span></span>

### <span data-ttu-id="fadd4-104">S1</span><span class="sxs-lookup"><span data-stu-id="fadd4-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fadd4-105">S2</span><span class="sxs-lookup"><span data-stu-id="fadd4-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fadd4-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="fadd4-106">DESCRIPTION</span></span>
<span data-ttu-id="fadd4-107">A **Remove-AzureRmWebAppSlot** parancsmag eltávolít egy Azure Web App-bővítőhelyet, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fadd4-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="fadd4-108">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="fadd4-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="fadd4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fadd4-109">EXAMPLES</span></span>

### <span data-ttu-id="fadd4-110">1. példa: webalkalmazás-bővítőhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fadd4-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="fadd4-111">Ez a parancs eltávolítja a Slot001-hoz társított, a ContosoSite nevű bővítőhelyet, amely a Default-Web-WestUS nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="fadd4-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fadd4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fadd4-112">PARAMETERS</span></span>

### <span data-ttu-id="fadd4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fadd4-113">-Force</span></span>
<span data-ttu-id="fadd4-114">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="fadd4-114">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="fadd4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fadd4-115">-Name</span></span>
<span data-ttu-id="fadd4-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="fadd4-116">WebApp Name</span></span>

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

### <span data-ttu-id="fadd4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fadd4-117">-ResourceGroupName</span></span>
<span data-ttu-id="fadd4-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="fadd4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="fadd4-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="fadd4-119">-Slot</span></span>
<span data-ttu-id="fadd4-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="fadd4-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadd4-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fadd4-121">-WebApp</span></span>
<span data-ttu-id="fadd4-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="fadd4-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fadd4-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fadd4-123">-Confirm</span></span>
<span data-ttu-id="fadd4-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fadd4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fadd4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fadd4-125">-WhatIf</span></span>
<span data-ttu-id="fadd4-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fadd4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fadd4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fadd4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fadd4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadd4-128">-DefaultProfile</span></span>
<span data-ttu-id="fadd4-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fadd4-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fadd4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadd4-130">CommonParameters</span></span>
<span data-ttu-id="fadd4-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fadd4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadd4-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fadd4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadd4-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fadd4-133">INPUTS</span></span>

### <span data-ttu-id="fadd4-134">Webhely</span><span class="sxs-lookup"><span data-stu-id="fadd4-134">Site</span></span>
<span data-ttu-id="fadd4-135">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fadd4-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fadd4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fadd4-136">OUTPUTS</span></span>

### <span data-ttu-id="fadd4-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fadd4-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="fadd4-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fadd4-138">NOTES</span></span>

## <span data-ttu-id="fadd4-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fadd4-139">RELATED LINKS</span></span>

[<span data-ttu-id="fadd4-140">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fadd4-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="fadd4-141">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fadd4-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="fadd4-142">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fadd4-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="fadd4-143">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fadd4-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="fadd4-144">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fadd4-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="fadd4-145">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fadd4-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="fadd4-146">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fadd4-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
