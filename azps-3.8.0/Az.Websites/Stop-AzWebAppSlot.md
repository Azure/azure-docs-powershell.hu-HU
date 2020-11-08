---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012584"
---
# <span data-ttu-id="d0583-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d0583-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="d0583-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0583-102">SYNOPSIS</span></span>
<span data-ttu-id="d0583-103">Azure Web App-bővítőhely leállítása</span><span class="sxs-lookup"><span data-stu-id="d0583-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="d0583-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0583-104">SYNTAX</span></span>

### <span data-ttu-id="d0583-105">S1</span><span class="sxs-lookup"><span data-stu-id="d0583-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0583-106">S2</span><span class="sxs-lookup"><span data-stu-id="d0583-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0583-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0583-107">DESCRIPTION</span></span>
<span data-ttu-id="d0583-108">A **stop-AzWebAppSlot** parancsmag egy Azure Web App-bővítőhelyet állít le.</span><span class="sxs-lookup"><span data-stu-id="d0583-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="d0583-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d0583-109">EXAMPLES</span></span>

### <span data-ttu-id="d0583-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d0583-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d0583-111">Ez a parancs leállítja a ContosoWebApp nevű Slot001 tartozó, a Default-Web-WestUS nevű erőforráscsoport számára tartozó bővítőhelyet.</span><span class="sxs-lookup"><span data-stu-id="d0583-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d0583-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0583-112">PARAMETERS</span></span>

### <span data-ttu-id="d0583-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0583-113">-DefaultProfile</span></span>
<span data-ttu-id="d0583-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0583-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0583-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0583-115">-Name</span></span>
<span data-ttu-id="d0583-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="d0583-116">WebApp Name</span></span>

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

### <span data-ttu-id="d0583-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0583-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0583-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d0583-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d0583-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="d0583-119">-Slot</span></span>
<span data-ttu-id="d0583-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="d0583-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d0583-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d0583-121">-WebApp</span></span>
<span data-ttu-id="d0583-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="d0583-122">WebApp Object</span></span>

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

### <span data-ttu-id="d0583-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0583-123">CommonParameters</span></span>
<span data-ttu-id="d0583-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0583-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0583-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0583-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0583-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0583-126">INPUTS</span></span>

### <span data-ttu-id="d0583-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d0583-127">System.String</span></span>

### <span data-ttu-id="d0583-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d0583-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d0583-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0583-129">OUTPUTS</span></span>

### <span data-ttu-id="d0583-130">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d0583-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d0583-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0583-131">NOTES</span></span>

## <span data-ttu-id="d0583-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0583-132">RELATED LINKS</span></span>
