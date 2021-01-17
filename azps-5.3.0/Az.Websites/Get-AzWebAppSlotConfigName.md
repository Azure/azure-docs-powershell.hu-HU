---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467021"
---
# <span data-ttu-id="4cb7b-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="4cb7b-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="4cb7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb7b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb7b-103">A Web App Slot config-nevek listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="4cb7b-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="4cb7b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4cb7b-104">SYNTAX</span></span>

### <span data-ttu-id="4cb7b-105">S1</span><span class="sxs-lookup"><span data-stu-id="4cb7b-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cb7b-106">S2</span><span class="sxs-lookup"><span data-stu-id="4cb7b-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cb7b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4cb7b-107">DESCRIPTION</span></span>
<span data-ttu-id="4cb7b-108">A **Get-AzWebAppSlotConfigName** parancsmag beolvassa a jelenleg slot-beállításként megjelölt alkalmazásbeállítás- és kapcsolati karakterláncnevek listáját.</span><span class="sxs-lookup"><span data-stu-id="4cb7b-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="4cb7b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4cb7b-109">EXAMPLES</span></span>

### <span data-ttu-id="4cb7b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4cb7b-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="4cb7b-111">Ez a parancs a Default-Web-WestUS erőforráscsoporttal társított ContosoSite nevű webalkalmazásra vonatkozó alkalmazásbeállításokat és kapcsolati karakterláncokat kapja</span><span class="sxs-lookup"><span data-stu-id="4cb7b-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4cb7b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cb7b-112">PARAMETERS</span></span>

### <span data-ttu-id="4cb7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb7b-113">-DefaultProfile</span></span>
<span data-ttu-id="4cb7b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4cb7b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cb7b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4cb7b-115">-Name</span></span>
<span data-ttu-id="4cb7b-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="4cb7b-116">WebApp Name</span></span>

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

### <span data-ttu-id="4cb7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4cb7b-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4cb7b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4cb7b-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4cb7b-119">-WebApp</span></span>
<span data-ttu-id="4cb7b-120">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="4cb7b-120">WebApp Object</span></span>

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

### <span data-ttu-id="4cb7b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb7b-121">CommonParameters</span></span>
<span data-ttu-id="4cb7b-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb7b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb7b-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cb7b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb7b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4cb7b-124">INPUTS</span></span>

### <span data-ttu-id="4cb7b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4cb7b-125">System.String</span></span>

### <span data-ttu-id="4cb7b-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4cb7b-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4cb7b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cb7b-127">OUTPUTS</span></span>

### <span data-ttu-id="4cb7b-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="4cb7b-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="4cb7b-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4cb7b-129">NOTES</span></span>

## <span data-ttu-id="4cb7b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4cb7b-130">RELATED LINKS</span></span>
