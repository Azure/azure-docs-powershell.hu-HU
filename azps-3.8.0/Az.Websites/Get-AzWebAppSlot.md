---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012011"
---
# <span data-ttu-id="81562-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81562-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="81562-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81562-102">SYNOPSIS</span></span>
<span data-ttu-id="81562-103">Azure Web App-bővítőhelyet kap.</span><span class="sxs-lookup"><span data-stu-id="81562-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="81562-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81562-104">SYNTAX</span></span>

### <span data-ttu-id="81562-105">S1</span><span class="sxs-lookup"><span data-stu-id="81562-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81562-106">S2</span><span class="sxs-lookup"><span data-stu-id="81562-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81562-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81562-107">DESCRIPTION</span></span>
<span data-ttu-id="81562-108">A **Get-AzWebAppSlot** parancsmag információt kap egy Azure Web App-bővítőhelyről.</span><span class="sxs-lookup"><span data-stu-id="81562-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="81562-109">Példák</span><span class="sxs-lookup"><span data-stu-id="81562-109">EXAMPLES</span></span>

### <span data-ttu-id="81562-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81562-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="81562-111">Ez a parancs beolvassa a Slot001 nevű bővítőhelyet a WebAppStandard nevű webalkalmazásból, amely az erőforráscsoport alapértelmezett – webes WestUS tartozik.</span><span class="sxs-lookup"><span data-stu-id="81562-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="81562-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81562-112">PARAMETERS</span></span>

### <span data-ttu-id="81562-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81562-113">-DefaultProfile</span></span>
<span data-ttu-id="81562-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81562-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81562-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81562-115">-Name</span></span>
<span data-ttu-id="81562-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="81562-116">WebApp Name</span></span>

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

### <span data-ttu-id="81562-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81562-117">-ResourceGroupName</span></span>
<span data-ttu-id="81562-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="81562-118">Resource Group Name</span></span>

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

### <span data-ttu-id="81562-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="81562-119">-Slot</span></span>
<span data-ttu-id="81562-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="81562-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81562-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="81562-121">-WebApp</span></span>
<span data-ttu-id="81562-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="81562-122">WebApp Object</span></span>

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

### <span data-ttu-id="81562-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81562-123">CommonParameters</span></span>
<span data-ttu-id="81562-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81562-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81562-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81562-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81562-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81562-126">INPUTS</span></span>

### <span data-ttu-id="81562-127">System. String</span><span class="sxs-lookup"><span data-stu-id="81562-127">System.String</span></span>

### <span data-ttu-id="81562-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="81562-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="81562-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81562-129">OUTPUTS</span></span>

### <span data-ttu-id="81562-130">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="81562-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="81562-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81562-131">NOTES</span></span>

## <span data-ttu-id="81562-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81562-132">RELATED LINKS</span></span>

[<span data-ttu-id="81562-133">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81562-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="81562-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81562-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="81562-135">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81562-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="81562-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81562-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="81562-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81562-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="81562-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81562-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="81562-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="81562-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
