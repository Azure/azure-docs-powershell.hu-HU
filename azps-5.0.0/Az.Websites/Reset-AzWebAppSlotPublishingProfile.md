---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194956"
---
# <span data-ttu-id="c62c6-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c62c6-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="c62c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c62c6-102">SYNOPSIS</span></span>

## <span data-ttu-id="c62c6-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c62c6-103">SYNTAX</span></span>

### <span data-ttu-id="c62c6-104">S1</span><span class="sxs-lookup"><span data-stu-id="c62c6-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c62c6-105">S2</span><span class="sxs-lookup"><span data-stu-id="c62c6-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c62c6-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="c62c6-106">DESCRIPTION</span></span>
<span data-ttu-id="c62c6-107">A **reset-AzWebAppSlotPublishingProfile** parancsmag visszaállítja a megadott webalkalmazás-bővítőhely közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="c62c6-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="c62c6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c62c6-108">EXAMPLES</span></span>

### <span data-ttu-id="c62c6-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c62c6-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="c62c6-110">Ez a parancs visszaállítja a slot001 nevű bővítőhely közzétételi profilját az erőforráscsoport alapértelmezett ContosoWebApp társított, a web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c62c6-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c62c6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c62c6-111">PARAMETERS</span></span>

### <span data-ttu-id="c62c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62c6-112">-DefaultProfile</span></span>
<span data-ttu-id="c62c6-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c62c6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c62c6-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c62c6-114">-Name</span></span>
<span data-ttu-id="c62c6-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c62c6-115">WebApp Name</span></span>

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

### <span data-ttu-id="c62c6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62c6-116">-ResourceGroupName</span></span>
<span data-ttu-id="c62c6-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c62c6-117">Resource Group Name</span></span>

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

### <span data-ttu-id="c62c6-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="c62c6-118">-Slot</span></span>
<span data-ttu-id="c62c6-119">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="c62c6-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c62c6-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c62c6-120">-WebApp</span></span>
<span data-ttu-id="c62c6-121">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c62c6-121">WebApp Object</span></span>

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

### <span data-ttu-id="c62c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62c6-122">CommonParameters</span></span>
<span data-ttu-id="c62c6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c62c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62c6-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c62c6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62c6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c62c6-125">INPUTS</span></span>

### <span data-ttu-id="c62c6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c62c6-126">System.String</span></span>

### <span data-ttu-id="c62c6-127">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c62c6-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c62c6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c62c6-128">OUTPUTS</span></span>

### <span data-ttu-id="c62c6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c62c6-129">System.String</span></span>

## <span data-ttu-id="c62c6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c62c6-130">NOTES</span></span>

## <span data-ttu-id="c62c6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c62c6-131">RELATED LINKS</span></span>