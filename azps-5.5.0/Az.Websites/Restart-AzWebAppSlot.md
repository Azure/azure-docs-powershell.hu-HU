---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164466"
---
# <span data-ttu-id="1d31a-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d31a-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="1d31a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d31a-102">SYNOPSIS</span></span>

## <span data-ttu-id="1d31a-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d31a-103">SYNTAX</span></span>

### <span data-ttu-id="1d31a-104">S1</span><span class="sxs-lookup"><span data-stu-id="1d31a-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d31a-105">S2</span><span class="sxs-lookup"><span data-stu-id="1d31a-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d31a-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d31a-106">DESCRIPTION</span></span>
<span data-ttu-id="1d31a-107">Az **Restart-AzWebAppSzaj** parancsmag leáll, majd elindít egy Azure Web App Slotot.</span><span class="sxs-lookup"><span data-stu-id="1d31a-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="1d31a-108">Ha a Web App Slot leállt állapotban van, használja a Start-AzWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1d31a-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="1d31a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d31a-109">EXAMPLES</span></span>

### <span data-ttu-id="1d31a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="1d31a-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="1d31a-111">Ez a parancs újraindítja a Default-Web-WestUS erőforráscsoporthoz társított ContosoWebApp webapp slot Slot001-et</span><span class="sxs-lookup"><span data-stu-id="1d31a-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1d31a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d31a-112">PARAMETERS</span></span>

### <span data-ttu-id="1d31a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d31a-113">-DefaultProfile</span></span>
<span data-ttu-id="1d31a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d31a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d31a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1d31a-115">-Name</span></span>
<span data-ttu-id="1d31a-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="1d31a-116">WebApp Name</span></span>

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

### <span data-ttu-id="1d31a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d31a-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d31a-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1d31a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1d31a-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="1d31a-119">-Slot</span></span>
<span data-ttu-id="1d31a-120">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="1d31a-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1d31a-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1d31a-121">-WebApp</span></span>
<span data-ttu-id="1d31a-122">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="1d31a-122">WebApp Object</span></span>

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

### <span data-ttu-id="1d31a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d31a-123">CommonParameters</span></span>
<span data-ttu-id="1d31a-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d31a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d31a-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d31a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d31a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d31a-126">INPUTS</span></span>

### <span data-ttu-id="1d31a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1d31a-127">System.String</span></span>

### <span data-ttu-id="1d31a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1d31a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1d31a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d31a-129">OUTPUTS</span></span>

### <span data-ttu-id="1d31a-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1d31a-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1d31a-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d31a-131">NOTES</span></span>

## <span data-ttu-id="1d31a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d31a-132">RELATED LINKS</span></span>

[<span data-ttu-id="1d31a-133">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="1d31a-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="1d31a-134">New-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="1d31a-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="1d31a-135">Remove-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="1d31a-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="1d31a-136">Set-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="1d31a-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="1d31a-137">Start-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="1d31a-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="1d31a-138">Stop-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="1d31a-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="1d31a-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1d31a-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
