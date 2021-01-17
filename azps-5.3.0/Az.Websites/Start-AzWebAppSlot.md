---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466957"
---
# <span data-ttu-id="a987d-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a987d-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="a987d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a987d-102">SYNOPSIS</span></span>
<span data-ttu-id="a987d-103">Elindít egy Azure Web App-helyet.</span><span class="sxs-lookup"><span data-stu-id="a987d-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="a987d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a987d-104">SYNTAX</span></span>

### <span data-ttu-id="a987d-105">S1</span><span class="sxs-lookup"><span data-stu-id="a987d-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a987d-106">S2</span><span class="sxs-lookup"><span data-stu-id="a987d-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a987d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a987d-107">DESCRIPTION</span></span>
<span data-ttu-id="a987d-108">A **Start-AzWebAppSzaj** parancsmag elindít egy Azure Web App Slotot.</span><span class="sxs-lookup"><span data-stu-id="a987d-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="a987d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a987d-109">EXAMPLES</span></span>

### <span data-ttu-id="a987d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a987d-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="a987d-111">Ez a parancs elindítja a Slot001 nevű slotot a Default-Web-WestUS nevű erőforráscsoporthoz tartozó ContosoWebApp nevű webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="a987d-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a987d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a987d-112">PARAMETERS</span></span>

### <span data-ttu-id="a987d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a987d-113">-DefaultProfile</span></span>
<span data-ttu-id="a987d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a987d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a987d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a987d-115">-Name</span></span>
<span data-ttu-id="a987d-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="a987d-116">WebApp Name</span></span>

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

### <span data-ttu-id="a987d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a987d-117">-ResourceGroupName</span></span>
<span data-ttu-id="a987d-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a987d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a987d-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="a987d-119">-Slot</span></span>
<span data-ttu-id="a987d-120">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="a987d-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a987d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a987d-121">-WebApp</span></span>
<span data-ttu-id="a987d-122">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="a987d-122">WebApp Object</span></span>

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

### <span data-ttu-id="a987d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a987d-123">CommonParameters</span></span>
<span data-ttu-id="a987d-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a987d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a987d-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a987d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a987d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a987d-126">INPUTS</span></span>

### <span data-ttu-id="a987d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a987d-127">System.String</span></span>

### <span data-ttu-id="a987d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a987d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a987d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a987d-129">OUTPUTS</span></span>

### <span data-ttu-id="a987d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a987d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a987d-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a987d-131">NOTES</span></span>

## <span data-ttu-id="a987d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a987d-132">RELATED LINKS</span></span>

[<span data-ttu-id="a987d-133">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a987d-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="a987d-134">New-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a987d-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="a987d-135">Remove-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a987d-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="a987d-136">Restart-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a987d-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="a987d-137">Set-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a987d-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="a987d-138">Stop-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="a987d-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="a987d-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a987d-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
