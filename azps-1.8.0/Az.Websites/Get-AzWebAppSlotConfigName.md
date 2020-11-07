---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: bd871e75e5a4f9c8e5c28e8788c8ef291a88e6db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668345"
---
# <span data-ttu-id="ab840-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="ab840-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="ab840-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab840-102">SYNOPSIS</span></span>
<span data-ttu-id="ab840-103">A Web App-bővítőhely konfigurációs neveinek listája</span><span class="sxs-lookup"><span data-stu-id="ab840-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="ab840-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab840-104">SYNTAX</span></span>

### <span data-ttu-id="ab840-105">S1</span><span class="sxs-lookup"><span data-stu-id="ab840-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab840-106">S2</span><span class="sxs-lookup"><span data-stu-id="ab840-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab840-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab840-107">DESCRIPTION</span></span>
<span data-ttu-id="ab840-108">A **Get-AzWebAppSlotConfigName** parancsmag kikeresi az app beállításai és a kapcsolati karakterláncok listáját, amelyek jelenleg a bővítőhelyek beállításai szerint vannak megjelölve</span><span class="sxs-lookup"><span data-stu-id="ab840-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="ab840-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ab840-109">EXAMPLES</span></span>

### <span data-ttu-id="ab840-110">1:</span><span class="sxs-lookup"><span data-stu-id="ab840-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ab840-111">Ez a parancs az App beállításaival és a kapcsolati karakterláncokkal függ össze az ContosoSite társított, az erőforráscsoport alapértelmezett verziójának – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="ab840-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ab840-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab840-112">PARAMETERS</span></span>

### <span data-ttu-id="ab840-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab840-113">-DefaultProfile</span></span>
<span data-ttu-id="ab840-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab840-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab840-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab840-115">-Name</span></span>
<span data-ttu-id="ab840-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="ab840-116">WebApp Name</span></span>

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

### <span data-ttu-id="ab840-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab840-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab840-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ab840-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ab840-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ab840-119">-WebApp</span></span>
<span data-ttu-id="ab840-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="ab840-120">WebApp Object</span></span>

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

### <span data-ttu-id="ab840-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab840-121">CommonParameters</span></span>
<span data-ttu-id="ab840-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab840-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab840-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab840-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab840-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab840-124">INPUTS</span></span>

### <span data-ttu-id="ab840-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ab840-125">System.String</span></span>

### <span data-ttu-id="ab840-126">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ab840-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ab840-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab840-127">OUTPUTS</span></span>

### <span data-ttu-id="ab840-128">Microsoft. Azure. Management. WebSites. models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="ab840-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="ab840-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab840-129">NOTES</span></span>

## <span data-ttu-id="ab840-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab840-130">RELATED LINKS</span></span>
