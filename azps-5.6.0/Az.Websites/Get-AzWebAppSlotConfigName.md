---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 2157c7a570f38838a65e1d4bba40dade22e10367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923898"
---
# <span data-ttu-id="69fe7-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="69fe7-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="69fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="69fe7-103">A Web App Slot config-nevek listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="69fe7-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="69fe7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69fe7-104">SYNTAX</span></span>

### <span data-ttu-id="69fe7-105">S1</span><span class="sxs-lookup"><span data-stu-id="69fe7-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe7-106">S2</span><span class="sxs-lookup"><span data-stu-id="69fe7-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69fe7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69fe7-107">DESCRIPTION</span></span>
<span data-ttu-id="69fe7-108">A **Get-AzWebAppSlotConfigName** parancsmag beolvassa a jelenleg slot-beállításként megjelölt alkalmazásbeállítás- és kapcsolati karakterláncnevek listáját.</span><span class="sxs-lookup"><span data-stu-id="69fe7-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="69fe7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69fe7-109">EXAMPLES</span></span>

### <span data-ttu-id="69fe7-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="69fe7-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="69fe7-111">Ez a parancs a Default-Web-WestUS erőforráscsoporttal társított ContosoSite nevű webalkalmazásra vonatkozó alkalmazásbeállításokat és kapcsolati karakterláncokat kapja</span><span class="sxs-lookup"><span data-stu-id="69fe7-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="69fe7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69fe7-112">PARAMETERS</span></span>

### <span data-ttu-id="69fe7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fe7-113">-DefaultProfile</span></span>
<span data-ttu-id="69fe7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69fe7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69fe7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="69fe7-115">-Name</span></span>
<span data-ttu-id="69fe7-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="69fe7-116">WebApp Name</span></span>

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

### <span data-ttu-id="69fe7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69fe7-117">-ResourceGroupName</span></span>
<span data-ttu-id="69fe7-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="69fe7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="69fe7-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="69fe7-119">-WebApp</span></span>
<span data-ttu-id="69fe7-120">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="69fe7-120">WebApp Object</span></span>

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

### <span data-ttu-id="69fe7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fe7-121">CommonParameters</span></span>
<span data-ttu-id="69fe7-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69fe7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fe7-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69fe7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fe7-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69fe7-124">INPUTS</span></span>

### <span data-ttu-id="69fe7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="69fe7-125">System.String</span></span>

### <span data-ttu-id="69fe7-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="69fe7-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="69fe7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69fe7-127">OUTPUTS</span></span>

### <span data-ttu-id="69fe7-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="69fe7-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="69fe7-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69fe7-129">NOTES</span></span>

## <span data-ttu-id="69fe7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69fe7-130">RELATED LINKS</span></span>
