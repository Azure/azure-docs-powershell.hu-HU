---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 7c443625294b3a23ac79dfcbabb724a2d3fceaa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928489"
---
# <span data-ttu-id="6cef9-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="6cef9-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="6cef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cef9-102">SYNOPSIS</span></span>
<span data-ttu-id="6cef9-103">Biztonsági beállítások lekérte az Azure Biztonsági központban</span><span class="sxs-lookup"><span data-stu-id="6cef9-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="6cef9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cef9-104">SYNTAX</span></span>

### <span data-ttu-id="6cef9-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cef9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cef9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="6cef9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cef9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cef9-107">DESCRIPTION</span></span>
<span data-ttu-id="6cef9-108">A Get-AzSecuritySetting parancsmag biztonsági beállításokat kap az Azure Biztonsági központban.</span><span class="sxs-lookup"><span data-stu-id="6cef9-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="6cef9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cef9-109">EXAMPLES</span></span>

### <span data-ttu-id="6cef9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="6cef9-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="6cef9-111">MCAS-adatexport beállítást kap</span><span class="sxs-lookup"><span data-stu-id="6cef9-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="6cef9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cef9-112">PARAMETERS</span></span>

### <span data-ttu-id="6cef9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cef9-113">-DefaultProfile</span></span>
<span data-ttu-id="6cef9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cef9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef9-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="6cef9-115">-SettingName</span></span>
<span data-ttu-id="6cef9-116">Beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="6cef9-116">Setting name.</span></span> <span data-ttu-id="6cef9-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="6cef9-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cef9-118">CommonParameters</span></span>
<span data-ttu-id="6cef9-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cef9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cef9-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cef9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cef9-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cef9-121">INPUTS</span></span>

### <span data-ttu-id="6cef9-122">System.String</span><span class="sxs-lookup"><span data-stu-id="6cef9-122">System.String</span></span>

## <span data-ttu-id="6cef9-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cef9-123">OUTPUTS</span></span>

### <span data-ttu-id="6cef9-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="6cef9-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="6cef9-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="6cef9-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="6cef9-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cef9-126">NOTES</span></span>

## <span data-ttu-id="6cef9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cef9-127">RELATED LINKS</span></span>
