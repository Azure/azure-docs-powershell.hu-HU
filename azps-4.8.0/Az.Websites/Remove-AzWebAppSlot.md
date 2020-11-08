---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025010"
---
# <span data-ttu-id="ab82a-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab82a-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="ab82a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab82a-102">SYNOPSIS</span></span>

## <span data-ttu-id="ab82a-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab82a-103">SYNTAX</span></span>

### <span data-ttu-id="ab82a-104">S1</span><span class="sxs-lookup"><span data-stu-id="ab82a-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab82a-105">S2</span><span class="sxs-lookup"><span data-stu-id="ab82a-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab82a-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab82a-106">DESCRIPTION</span></span>
<span data-ttu-id="ab82a-107">A **Remove-AzWebAppSlot** parancsmag eltávolít egy Azure Web App-bővítőhelyet, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab82a-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="ab82a-108">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ab82a-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="ab82a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ab82a-109">EXAMPLES</span></span>

### <span data-ttu-id="ab82a-110">1. példa: webalkalmazás-bővítőhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ab82a-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="ab82a-111">Ez a parancs eltávolítja a Slot001-hoz társított, a ContosoSite nevű bővítőhelyet, amely a Default-Web-WestUS nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="ab82a-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ab82a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab82a-112">PARAMETERS</span></span>

### <span data-ttu-id="ab82a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab82a-113">-AsJob</span></span>
<span data-ttu-id="ab82a-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ab82a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab82a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab82a-115">-DefaultProfile</span></span>
<span data-ttu-id="ab82a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab82a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab82a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ab82a-117">-Force</span></span>
<span data-ttu-id="ab82a-118">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="ab82a-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ab82a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab82a-119">-Name</span></span>
<span data-ttu-id="ab82a-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="ab82a-120">WebApp Name</span></span>

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

### <span data-ttu-id="ab82a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab82a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab82a-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ab82a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="ab82a-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="ab82a-123">-Slot</span></span>
<span data-ttu-id="ab82a-124">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="ab82a-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ab82a-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ab82a-125">-WebApp</span></span>
<span data-ttu-id="ab82a-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="ab82a-126">WebApp Object</span></span>

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

### <span data-ttu-id="ab82a-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab82a-127">-Confirm</span></span>
<span data-ttu-id="ab82a-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab82a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab82a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab82a-129">-WhatIf</span></span>
<span data-ttu-id="ab82a-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ab82a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab82a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab82a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab82a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab82a-132">CommonParameters</span></span>
<span data-ttu-id="ab82a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab82a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab82a-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab82a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab82a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab82a-135">INPUTS</span></span>

### <span data-ttu-id="ab82a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ab82a-136">System.String</span></span>

### <span data-ttu-id="ab82a-137">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ab82a-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ab82a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab82a-138">OUTPUTS</span></span>

### <span data-ttu-id="ab82a-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ab82a-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ab82a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab82a-140">NOTES</span></span>

## <span data-ttu-id="ab82a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab82a-141">RELATED LINKS</span></span>

[<span data-ttu-id="ab82a-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab82a-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="ab82a-143">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab82a-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="ab82a-144">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab82a-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="ab82a-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab82a-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="ab82a-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab82a-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="ab82a-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab82a-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="ab82a-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab82a-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
