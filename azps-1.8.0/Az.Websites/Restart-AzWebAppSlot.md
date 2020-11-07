---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 53323aaf29145f4340dd00fa752d8afd2dd72131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668306"
---
# <span data-ttu-id="c7fe4-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c7fe4-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="c7fe4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7fe4-102">SYNOPSIS</span></span>

## <span data-ttu-id="c7fe4-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7fe4-103">SYNTAX</span></span>

### <span data-ttu-id="c7fe4-104">S1</span><span class="sxs-lookup"><span data-stu-id="c7fe4-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7fe4-105">S2</span><span class="sxs-lookup"><span data-stu-id="c7fe4-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7fe4-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7fe4-106">DESCRIPTION</span></span>
<span data-ttu-id="c7fe4-107">Az **Újraindítás – AzWebAppSlot** parancsmag leáll, majd egy Azure Web App-bővítőhelyet indít el.</span><span class="sxs-lookup"><span data-stu-id="c7fe4-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="c7fe4-108">Ha a Web App a leállított állapotban van, használja az Start-AzWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c7fe4-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="c7fe4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c7fe4-109">EXAMPLES</span></span>

### <span data-ttu-id="c7fe4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c7fe4-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="c7fe4-111">Ez a parancs elindítja a Slot001 a ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának bővítőhelyét – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="c7fe4-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c7fe4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7fe4-112">PARAMETERS</span></span>

### <span data-ttu-id="c7fe4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fe4-113">-DefaultProfile</span></span>
<span data-ttu-id="c7fe4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7fe4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7fe4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7fe4-115">-Name</span></span>
<span data-ttu-id="c7fe4-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c7fe4-116">WebApp Name</span></span>

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

### <span data-ttu-id="c7fe4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7fe4-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7fe4-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c7fe4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c7fe4-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="c7fe4-119">-Slot</span></span>
<span data-ttu-id="c7fe4-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="c7fe4-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c7fe4-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c7fe4-121">-WebApp</span></span>
<span data-ttu-id="c7fe4-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c7fe4-122">WebApp Object</span></span>

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

### <span data-ttu-id="c7fe4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fe4-123">CommonParameters</span></span>
<span data-ttu-id="c7fe4-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7fe4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fe4-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7fe4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fe4-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7fe4-126">INPUTS</span></span>

### <span data-ttu-id="c7fe4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c7fe4-127">System.String</span></span>

### <span data-ttu-id="c7fe4-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c7fe4-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c7fe4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7fe4-129">OUTPUTS</span></span>

### <span data-ttu-id="c7fe4-130">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c7fe4-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c7fe4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7fe4-131">NOTES</span></span>

## <span data-ttu-id="c7fe4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7fe4-132">RELATED LINKS</span></span>

[<span data-ttu-id="c7fe4-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c7fe4-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c7fe4-134">Új – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c7fe4-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c7fe4-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c7fe4-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c7fe4-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c7fe4-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="c7fe4-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c7fe4-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c7fe4-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c7fe4-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c7fe4-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7fe4-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
