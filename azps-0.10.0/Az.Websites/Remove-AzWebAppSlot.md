---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842714"
---
# <span data-ttu-id="e3ddb-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3ddb-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="e3ddb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3ddb-102">SYNOPSIS</span></span>

## <span data-ttu-id="e3ddb-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3ddb-103">SYNTAX</span></span>

### <span data-ttu-id="e3ddb-104">S1</span><span class="sxs-lookup"><span data-stu-id="e3ddb-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3ddb-105">S2</span><span class="sxs-lookup"><span data-stu-id="e3ddb-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3ddb-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3ddb-106">DESCRIPTION</span></span>
<span data-ttu-id="e3ddb-107">A **Remove-AzWebAppSlot** parancsmag eltávolít egy Azure Web App-bővítőhelyet, amely az erőforráscsoport és a webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3ddb-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="e3ddb-108">Ez a parancsmag alapértelmezés szerint az összes bővítőhelyet és metrikát is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="e3ddb-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="e3ddb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e3ddb-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ddb-110">1. példa: webalkalmazás-bővítőhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e3ddb-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="e3ddb-111">Ez a parancs eltávolítja a Slot001-hoz társított, a ContosoSite nevű bővítőhelyet, amely a Default-Web-WestUS nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="e3ddb-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e3ddb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3ddb-112">PARAMETERS</span></span>

### <span data-ttu-id="e3ddb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ddb-113">-DefaultProfile</span></span>
<span data-ttu-id="e3ddb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3ddb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3ddb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e3ddb-115">-Force</span></span>
<span data-ttu-id="e3ddb-116">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="e3ddb-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e3ddb-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3ddb-117">-Name</span></span>
<span data-ttu-id="e3ddb-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e3ddb-118">WebApp Name</span></span>

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

### <span data-ttu-id="e3ddb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ddb-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3ddb-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e3ddb-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e3ddb-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="e3ddb-121">-Slot</span></span>
<span data-ttu-id="e3ddb-122">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="e3ddb-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="e3ddb-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e3ddb-123">-WebApp</span></span>
<span data-ttu-id="e3ddb-124">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="e3ddb-124">WebApp Object</span></span>

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

### <span data-ttu-id="e3ddb-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3ddb-125">-Confirm</span></span>
<span data-ttu-id="e3ddb-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3ddb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3ddb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ddb-127">-WhatIf</span></span>
<span data-ttu-id="e3ddb-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3ddb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ddb-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3ddb-129">The cmdlet is not run.</span></span>

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
### <span data-ttu-id="e3ddb-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3ddb-130">-AsJob</span></span>
<span data-ttu-id="e3ddb-131">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e3ddb-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3ddb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ddb-132">CommonParameters</span></span>
<span data-ttu-id="e3ddb-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3ddb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ddb-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ddb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ddb-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ddb-135">INPUTS</span></span>

### <span data-ttu-id="e3ddb-136">Webhely</span><span class="sxs-lookup"><span data-stu-id="e3ddb-136">Site</span></span>
<span data-ttu-id="e3ddb-137">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e3ddb-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e3ddb-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ddb-138">OUTPUTS</span></span>

### <span data-ttu-id="e3ddb-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e3ddb-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e3ddb-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3ddb-140">NOTES</span></span>

## <span data-ttu-id="e3ddb-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3ddb-141">RELATED LINKS</span></span>

[<span data-ttu-id="e3ddb-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3ddb-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e3ddb-143">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3ddb-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="e3ddb-144">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3ddb-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="e3ddb-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3ddb-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="e3ddb-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3ddb-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="e3ddb-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3ddb-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="e3ddb-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3ddb-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
