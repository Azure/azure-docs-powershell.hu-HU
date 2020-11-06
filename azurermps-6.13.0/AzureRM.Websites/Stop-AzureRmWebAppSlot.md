---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 2e6130b93a3c549ca84c2cb0a6a336f6afb177b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495567"
---
# <span data-ttu-id="19faa-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19faa-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="19faa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19faa-102">SYNOPSIS</span></span>
<span data-ttu-id="19faa-103">Azure Web App-bővítőhely leállítása</span><span class="sxs-lookup"><span data-stu-id="19faa-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19faa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19faa-104">SYNTAX</span></span>

### <span data-ttu-id="19faa-105">S1</span><span class="sxs-lookup"><span data-stu-id="19faa-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19faa-106">S2</span><span class="sxs-lookup"><span data-stu-id="19faa-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19faa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="19faa-107">DESCRIPTION</span></span>
<span data-ttu-id="19faa-108">A **stop-AzureRmWebAppSlot** parancsmag egy Azure Web App-bővítőhelyet állít le.</span><span class="sxs-lookup"><span data-stu-id="19faa-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="19faa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="19faa-109">EXAMPLES</span></span>

### <span data-ttu-id="19faa-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19faa-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="19faa-111">Ez a parancs leállítja a ContosoWebApp nevű Slot001 tartozó, a Default-Web-WestUS nevű erőforráscsoport számára tartozó bővítőhelyet.</span><span class="sxs-lookup"><span data-stu-id="19faa-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="19faa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19faa-112">PARAMETERS</span></span>

### <span data-ttu-id="19faa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19faa-113">-DefaultProfile</span></span>
<span data-ttu-id="19faa-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19faa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19faa-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19faa-115">-Name</span></span>
<span data-ttu-id="19faa-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="19faa-116">WebApp Name</span></span>

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

### <span data-ttu-id="19faa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19faa-117">-ResourceGroupName</span></span>
<span data-ttu-id="19faa-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="19faa-118">Resource Group Name</span></span>

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

### <span data-ttu-id="19faa-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="19faa-119">-Slot</span></span>
<span data-ttu-id="19faa-120">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="19faa-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="19faa-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="19faa-121">-WebApp</span></span>
<span data-ttu-id="19faa-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="19faa-122">WebApp Object</span></span>

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

### <span data-ttu-id="19faa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19faa-123">CommonParameters</span></span>
<span data-ttu-id="19faa-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19faa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19faa-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19faa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19faa-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19faa-126">INPUTS</span></span>

### <span data-ttu-id="19faa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="19faa-127">System.String</span></span>

### <span data-ttu-id="19faa-128">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="19faa-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="19faa-129">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19faa-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="19faa-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19faa-130">OUTPUTS</span></span>

### <span data-ttu-id="19faa-131">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="19faa-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="19faa-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19faa-132">NOTES</span></span>

## <span data-ttu-id="19faa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19faa-133">RELATED LINKS</span></span>
