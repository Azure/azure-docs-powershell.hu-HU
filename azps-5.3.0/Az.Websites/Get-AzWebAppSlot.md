---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467022"
---
# <span data-ttu-id="c126b-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c126b-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="c126b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c126b-102">SYNOPSIS</span></span>
<span data-ttu-id="c126b-103">Egy Azure Web App-slotot kap.</span><span class="sxs-lookup"><span data-stu-id="c126b-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="c126b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c126b-104">SYNTAX</span></span>

### <span data-ttu-id="c126b-105">S1</span><span class="sxs-lookup"><span data-stu-id="c126b-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c126b-106">S2</span><span class="sxs-lookup"><span data-stu-id="c126b-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c126b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c126b-107">DESCRIPTION</span></span>
<span data-ttu-id="c126b-108">A **Get-AzWebAppSzaj** parancsmag információt kap az Azure Web App Slotról.</span><span class="sxs-lookup"><span data-stu-id="c126b-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="c126b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c126b-109">EXAMPLES</span></span>

### <span data-ttu-id="c126b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c126b-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="c126b-111">Ez a parancs a Default-Web-WestUS erőforráscsoporthoz tartozó WebAppStandard nevű WebAppStandard webappból kapja meg a Slot001 nevű tárolóhelyet.</span><span class="sxs-lookup"><span data-stu-id="c126b-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c126b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c126b-112">PARAMETERS</span></span>

### <span data-ttu-id="c126b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c126b-113">-DefaultProfile</span></span>
<span data-ttu-id="c126b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c126b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c126b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c126b-115">-Name</span></span>
<span data-ttu-id="c126b-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c126b-116">WebApp Name</span></span>

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

### <span data-ttu-id="c126b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c126b-117">-ResourceGroupName</span></span>
<span data-ttu-id="c126b-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c126b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c126b-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="c126b-119">-Slot</span></span>
<span data-ttu-id="c126b-120">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="c126b-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c126b-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c126b-121">-WebApp</span></span>
<span data-ttu-id="c126b-122">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="c126b-122">WebApp Object</span></span>

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

### <span data-ttu-id="c126b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c126b-123">CommonParameters</span></span>
<span data-ttu-id="c126b-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c126b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c126b-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c126b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c126b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c126b-126">INPUTS</span></span>

### <span data-ttu-id="c126b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c126b-127">System.String</span></span>

### <span data-ttu-id="c126b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c126b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c126b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c126b-129">OUTPUTS</span></span>

### <span data-ttu-id="c126b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c126b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c126b-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c126b-131">NOTES</span></span>

## <span data-ttu-id="c126b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c126b-132">RELATED LINKS</span></span>

[<span data-ttu-id="c126b-133">New-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="c126b-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c126b-134">Remove-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="c126b-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c126b-135">Restart-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="c126b-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="c126b-136">Set-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="c126b-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="c126b-137">Start-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="c126b-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c126b-138">Stop-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="c126b-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c126b-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c126b-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
