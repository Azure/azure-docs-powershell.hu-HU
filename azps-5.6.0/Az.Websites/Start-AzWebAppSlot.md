---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: c65eac94a9c44b3b7272116bc0e0757291b121b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011077"
---
# <span data-ttu-id="559bb-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="559bb-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="559bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="559bb-102">SYNOPSIS</span></span>
<span data-ttu-id="559bb-103">Elindít egy Azure Web App-helyet.</span><span class="sxs-lookup"><span data-stu-id="559bb-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="559bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="559bb-104">SYNTAX</span></span>

### <span data-ttu-id="559bb-105">S1</span><span class="sxs-lookup"><span data-stu-id="559bb-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="559bb-106">S2</span><span class="sxs-lookup"><span data-stu-id="559bb-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="559bb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="559bb-107">DESCRIPTION</span></span>
<span data-ttu-id="559bb-108">A **Start-AzWebAppSzaj** parancsmag elindít egy Azure Web App Slotot.</span><span class="sxs-lookup"><span data-stu-id="559bb-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="559bb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="559bb-109">EXAMPLES</span></span>

### <span data-ttu-id="559bb-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="559bb-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="559bb-111">Ez a parancs elindítja a Slot001 nevű slotot a Default-Web-WestUS nevű erőforráscsoporthoz tartozó ContosoWebApp nevű webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="559bb-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="559bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="559bb-112">PARAMETERS</span></span>

### <span data-ttu-id="559bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559bb-113">-DefaultProfile</span></span>
<span data-ttu-id="559bb-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="559bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="559bb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="559bb-115">-Name</span></span>
<span data-ttu-id="559bb-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="559bb-116">WebApp Name</span></span>

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

### <span data-ttu-id="559bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="559bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="559bb-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="559bb-118">Resource Group Name</span></span>

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

### <span data-ttu-id="559bb-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="559bb-119">-Slot</span></span>
<span data-ttu-id="559bb-120">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="559bb-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="559bb-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="559bb-121">-WebApp</span></span>
<span data-ttu-id="559bb-122">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="559bb-122">WebApp Object</span></span>

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

### <span data-ttu-id="559bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559bb-123">CommonParameters</span></span>
<span data-ttu-id="559bb-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="559bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559bb-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="559bb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559bb-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="559bb-126">INPUTS</span></span>

### <span data-ttu-id="559bb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="559bb-127">System.String</span></span>

### <span data-ttu-id="559bb-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="559bb-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="559bb-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="559bb-129">OUTPUTS</span></span>

### <span data-ttu-id="559bb-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="559bb-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="559bb-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="559bb-131">NOTES</span></span>

## <span data-ttu-id="559bb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="559bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="559bb-133">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="559bb-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="559bb-134">New-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="559bb-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="559bb-135">Remove-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="559bb-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="559bb-136">Restart-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="559bb-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="559bb-137">Set-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="559bb-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="559bb-138">Stop-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="559bb-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="559bb-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="559bb-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
