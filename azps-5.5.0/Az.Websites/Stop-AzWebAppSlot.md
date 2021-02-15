---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164419"
---
# <span data-ttu-id="b5d23-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b5d23-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="b5d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d23-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d23-103">Leállítja az Azure Web App-tárolóhelyet.</span><span class="sxs-lookup"><span data-stu-id="b5d23-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="b5d23-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5d23-104">SYNTAX</span></span>

### <span data-ttu-id="b5d23-105">S1</span><span class="sxs-lookup"><span data-stu-id="b5d23-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5d23-106">S2</span><span class="sxs-lookup"><span data-stu-id="b5d23-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5d23-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5d23-107">DESCRIPTION</span></span>
<span data-ttu-id="b5d23-108">A **Stop-AzWebAppSzaj** parancsmag leállítja az Azure Web App Slotot.</span><span class="sxs-lookup"><span data-stu-id="b5d23-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="b5d23-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5d23-109">EXAMPLES</span></span>

### <span data-ttu-id="b5d23-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b5d23-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="b5d23-111">Ez a parancs leállítja a ContosoWebApp nevű webalkalmazáshoz tartozó slot Slot001 tárolóhelyet, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="b5d23-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b5d23-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5d23-112">PARAMETERS</span></span>

### <span data-ttu-id="b5d23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d23-113">-DefaultProfile</span></span>
<span data-ttu-id="b5d23-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5d23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5d23-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b5d23-115">-Name</span></span>
<span data-ttu-id="b5d23-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="b5d23-116">WebApp Name</span></span>

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

### <span data-ttu-id="b5d23-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d23-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5d23-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b5d23-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b5d23-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="b5d23-119">-Slot</span></span>
<span data-ttu-id="b5d23-120">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="b5d23-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b5d23-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b5d23-121">-WebApp</span></span>
<span data-ttu-id="b5d23-122">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="b5d23-122">WebApp Object</span></span>

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

### <span data-ttu-id="b5d23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d23-123">CommonParameters</span></span>
<span data-ttu-id="b5d23-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d23-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d23-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d23-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5d23-126">INPUTS</span></span>

### <span data-ttu-id="b5d23-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b5d23-127">System.String</span></span>

### <span data-ttu-id="b5d23-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b5d23-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b5d23-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5d23-129">OUTPUTS</span></span>

### <span data-ttu-id="b5d23-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b5d23-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b5d23-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5d23-131">NOTES</span></span>

## <span data-ttu-id="b5d23-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5d23-132">RELATED LINKS</span></span>
