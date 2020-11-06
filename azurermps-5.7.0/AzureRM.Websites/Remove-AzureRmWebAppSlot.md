---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: eeaeb43083a2b125147df5d91516b71bdff377a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502312"
---
# <span data-ttu-id="531fd-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="531fd-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="531fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="531fd-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="531fd-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="531fd-103">SYNTAX</span></span>

### <span data-ttu-id="531fd-104">S1</span><span class="sxs-lookup"><span data-stu-id="531fd-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="531fd-105">S2</span><span class="sxs-lookup"><span data-stu-id="531fd-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="531fd-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="531fd-106">DESCRIPTION</span></span>
<span data-ttu-id="531fd-107">A **Remove-AzureRmWebAppSlot** parancsmag eltávolít egy Azure Web App-bővítőhelyet, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="531fd-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="531fd-108">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="531fd-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="531fd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="531fd-109">EXAMPLES</span></span>

### <span data-ttu-id="531fd-110">1. példa: webalkalmazás-bővítőhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="531fd-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="531fd-111">Ez a parancs eltávolítja a Slot001-hoz társított, a ContosoSite nevű bővítőhelyet, amely a Default-Web-WestUS nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="531fd-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="531fd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="531fd-112">PARAMETERS</span></span>

### <span data-ttu-id="531fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531fd-113">-DefaultProfile</span></span>
<span data-ttu-id="531fd-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="531fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="531fd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="531fd-115">-Force</span></span>
<span data-ttu-id="531fd-116">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="531fd-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="531fd-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="531fd-117">-Name</span></span>
<span data-ttu-id="531fd-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="531fd-118">WebApp Name</span></span>

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

### <span data-ttu-id="531fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="531fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="531fd-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="531fd-120">Resource Group Name</span></span>

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

### <span data-ttu-id="531fd-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="531fd-121">-Slot</span></span>
<span data-ttu-id="531fd-122">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="531fd-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531fd-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="531fd-123">-WebApp</span></span>
<span data-ttu-id="531fd-124">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="531fd-124">WebApp Object</span></span>

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

### <span data-ttu-id="531fd-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="531fd-125">-Confirm</span></span>
<span data-ttu-id="531fd-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="531fd-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531fd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="531fd-127">-WhatIf</span></span>
<span data-ttu-id="531fd-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="531fd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="531fd-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="531fd-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="531fd-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="531fd-130">-AsJob</span></span>
<span data-ttu-id="531fd-131">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="531fd-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="531fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531fd-132">CommonParameters</span></span>
<span data-ttu-id="531fd-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="531fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531fd-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="531fd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531fd-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="531fd-135">INPUTS</span></span>

### <span data-ttu-id="531fd-136">Webhely</span><span class="sxs-lookup"><span data-stu-id="531fd-136">Site</span></span>
<span data-ttu-id="531fd-137">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="531fd-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="531fd-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="531fd-138">OUTPUTS</span></span>

### <span data-ttu-id="531fd-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="531fd-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="531fd-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="531fd-140">NOTES</span></span>

## <span data-ttu-id="531fd-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="531fd-141">RELATED LINKS</span></span>

[<span data-ttu-id="531fd-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="531fd-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="531fd-143">Új – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="531fd-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="531fd-144">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="531fd-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="531fd-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="531fd-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="531fd-146">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="531fd-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="531fd-147">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="531fd-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="531fd-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="531fd-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
