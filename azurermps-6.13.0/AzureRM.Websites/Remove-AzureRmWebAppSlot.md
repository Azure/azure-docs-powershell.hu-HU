---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497176"
---
# <span data-ttu-id="924ce-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="924ce-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="924ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="924ce-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="924ce-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="924ce-103">SYNTAX</span></span>

### <span data-ttu-id="924ce-104">S1</span><span class="sxs-lookup"><span data-stu-id="924ce-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924ce-105">S2</span><span class="sxs-lookup"><span data-stu-id="924ce-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="924ce-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="924ce-106">DESCRIPTION</span></span>
<span data-ttu-id="924ce-107">A **Remove-AzureRmWebAppSlot** parancsmag eltávolít egy Azure Web App-bővítőhelyet, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="924ce-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="924ce-108">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="924ce-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="924ce-109">Példák</span><span class="sxs-lookup"><span data-stu-id="924ce-109">EXAMPLES</span></span>

### <span data-ttu-id="924ce-110">1. példa: webalkalmazás-bővítőhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="924ce-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="924ce-111">Ez a parancs eltávolítja a Slot001-hoz társított, a ContosoSite nevű bővítőhelyet, amely a Default-Web-WestUS nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="924ce-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="924ce-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="924ce-112">PARAMETERS</span></span>

### <span data-ttu-id="924ce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="924ce-113">-AsJob</span></span>
<span data-ttu-id="924ce-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="924ce-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="924ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924ce-115">-DefaultProfile</span></span>
<span data-ttu-id="924ce-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="924ce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="924ce-117">-Force</span><span class="sxs-lookup"><span data-stu-id="924ce-117">-Force</span></span>
<span data-ttu-id="924ce-118">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="924ce-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="924ce-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="924ce-119">-Name</span></span>
<span data-ttu-id="924ce-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="924ce-120">WebApp Name</span></span>

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

### <span data-ttu-id="924ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="924ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="924ce-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="924ce-122">Resource Group Name</span></span>

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

### <span data-ttu-id="924ce-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="924ce-123">-Slot</span></span>
<span data-ttu-id="924ce-124">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="924ce-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="924ce-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="924ce-125">-WebApp</span></span>
<span data-ttu-id="924ce-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="924ce-126">WebApp Object</span></span>

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

### <span data-ttu-id="924ce-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="924ce-127">-Confirm</span></span>
<span data-ttu-id="924ce-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="924ce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="924ce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="924ce-129">-WhatIf</span></span>
<span data-ttu-id="924ce-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="924ce-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="924ce-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="924ce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="924ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924ce-132">CommonParameters</span></span>
<span data-ttu-id="924ce-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="924ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924ce-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="924ce-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924ce-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="924ce-135">INPUTS</span></span>

### <span data-ttu-id="924ce-136">System. String</span><span class="sxs-lookup"><span data-stu-id="924ce-136">System.String</span></span>

### <span data-ttu-id="924ce-137">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="924ce-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="924ce-138">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="924ce-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="924ce-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="924ce-139">OUTPUTS</span></span>

### <span data-ttu-id="924ce-140">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="924ce-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="924ce-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="924ce-141">NOTES</span></span>

## <span data-ttu-id="924ce-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="924ce-142">RELATED LINKS</span></span>

[<span data-ttu-id="924ce-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="924ce-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="924ce-144">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="924ce-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="924ce-145">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="924ce-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="924ce-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="924ce-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="924ce-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="924ce-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="924ce-148">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="924ce-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="924ce-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="924ce-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
