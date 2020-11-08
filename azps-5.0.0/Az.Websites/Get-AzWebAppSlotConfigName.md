---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187129"
---
# <span data-ttu-id="58cdb-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="58cdb-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="58cdb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="58cdb-103">A Web App-bővítőhely konfigurációs neveinek listája</span><span class="sxs-lookup"><span data-stu-id="58cdb-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="58cdb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58cdb-104">SYNTAX</span></span>

### <span data-ttu-id="58cdb-105">S1</span><span class="sxs-lookup"><span data-stu-id="58cdb-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58cdb-106">S2</span><span class="sxs-lookup"><span data-stu-id="58cdb-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58cdb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="58cdb-107">DESCRIPTION</span></span>
<span data-ttu-id="58cdb-108">A **Get-AzWebAppSlotConfigName** parancsmag kikeresi az app beállításai és a kapcsolati karakterláncok listáját, amelyek jelenleg a bővítőhelyek beállításai szerint vannak megjelölve</span><span class="sxs-lookup"><span data-stu-id="58cdb-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="58cdb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="58cdb-109">EXAMPLES</span></span>

### <span data-ttu-id="58cdb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="58cdb-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="58cdb-111">Ez a parancs az App beállításaival és a kapcsolati karakterláncokkal függ össze az ContosoSite társított, az erőforráscsoport alapértelmezett verziójának – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="58cdb-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="58cdb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58cdb-112">PARAMETERS</span></span>

### <span data-ttu-id="58cdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58cdb-113">-DefaultProfile</span></span>
<span data-ttu-id="58cdb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58cdb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58cdb-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="58cdb-115">-Name</span></span>
<span data-ttu-id="58cdb-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="58cdb-116">WebApp Name</span></span>

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

### <span data-ttu-id="58cdb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58cdb-117">-ResourceGroupName</span></span>
<span data-ttu-id="58cdb-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="58cdb-118">Resource Group Name</span></span>

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

### <span data-ttu-id="58cdb-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="58cdb-119">-WebApp</span></span>
<span data-ttu-id="58cdb-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="58cdb-120">WebApp Object</span></span>

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

### <span data-ttu-id="58cdb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58cdb-121">CommonParameters</span></span>
<span data-ttu-id="58cdb-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58cdb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58cdb-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58cdb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58cdb-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58cdb-124">INPUTS</span></span>

### <span data-ttu-id="58cdb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="58cdb-125">System.String</span></span>

### <span data-ttu-id="58cdb-126">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="58cdb-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="58cdb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58cdb-127">OUTPUTS</span></span>

### <span data-ttu-id="58cdb-128">Microsoft. Azure. Management. WebSites. models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="58cdb-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="58cdb-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58cdb-129">NOTES</span></span>

## <span data-ttu-id="58cdb-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58cdb-130">RELATED LINKS</span></span>
