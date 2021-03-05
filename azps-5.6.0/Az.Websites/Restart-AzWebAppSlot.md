---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 75bedf4546bee73767c0488f578cdb5e17c1b745
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002085"
---
# <span data-ttu-id="22a95-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="22a95-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="22a95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22a95-102">SYNOPSIS</span></span>

## <span data-ttu-id="22a95-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22a95-103">SYNTAX</span></span>

### <span data-ttu-id="22a95-104">S1</span><span class="sxs-lookup"><span data-stu-id="22a95-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22a95-105">S2</span><span class="sxs-lookup"><span data-stu-id="22a95-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22a95-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22a95-106">DESCRIPTION</span></span>
<span data-ttu-id="22a95-107">Az **Restart-AzWebAppSzaj** parancsmag leáll, majd elindít egy Azure Web App Slotot.</span><span class="sxs-lookup"><span data-stu-id="22a95-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="22a95-108">Ha a Web App Slot leállt állapotban van, használja a Start-AzWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="22a95-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="22a95-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22a95-109">EXAMPLES</span></span>

### <span data-ttu-id="22a95-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="22a95-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="22a95-111">Ez a parancs újraindítja a Default-Web-WestUS erőforráscsoporthoz társított ContosoWebApp webapp slot Slot001-et</span><span class="sxs-lookup"><span data-stu-id="22a95-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="22a95-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22a95-112">PARAMETERS</span></span>

### <span data-ttu-id="22a95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a95-113">-DefaultProfile</span></span>
<span data-ttu-id="22a95-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22a95-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a95-115">-Name</span><span class="sxs-lookup"><span data-stu-id="22a95-115">-Name</span></span>
<span data-ttu-id="22a95-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="22a95-116">WebApp Name</span></span>

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

### <span data-ttu-id="22a95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a95-117">-ResourceGroupName</span></span>
<span data-ttu-id="22a95-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="22a95-118">Resource Group Name</span></span>

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

### <span data-ttu-id="22a95-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="22a95-119">-Slot</span></span>
<span data-ttu-id="22a95-120">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="22a95-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="22a95-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="22a95-121">-WebApp</span></span>
<span data-ttu-id="22a95-122">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="22a95-122">WebApp Object</span></span>

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

### <span data-ttu-id="22a95-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a95-123">CommonParameters</span></span>
<span data-ttu-id="22a95-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a95-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a95-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a95-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a95-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22a95-126">INPUTS</span></span>

### <span data-ttu-id="22a95-127">System.String</span><span class="sxs-lookup"><span data-stu-id="22a95-127">System.String</span></span>

### <span data-ttu-id="22a95-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="22a95-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="22a95-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22a95-129">OUTPUTS</span></span>

### <span data-ttu-id="22a95-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="22a95-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="22a95-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22a95-131">NOTES</span></span>

## <span data-ttu-id="22a95-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22a95-132">RELATED LINKS</span></span>

[<span data-ttu-id="22a95-133">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="22a95-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="22a95-134">New-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="22a95-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="22a95-135">Remove-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="22a95-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="22a95-136">Set-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="22a95-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="22a95-137">Start-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="22a95-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="22a95-138">Stop-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="22a95-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="22a95-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="22a95-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
