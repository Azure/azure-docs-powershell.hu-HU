---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156370"
---
# <span data-ttu-id="c33c2-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c33c2-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="c33c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c33c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c33c2-103">Biztonsági beállítások lekérte az Azure Biztonsági központban</span><span class="sxs-lookup"><span data-stu-id="c33c2-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="c33c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c33c2-104">SYNTAX</span></span>

### <span data-ttu-id="c33c2-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c33c2-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c33c2-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c33c2-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c33c2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c33c2-107">DESCRIPTION</span></span>
<span data-ttu-id="c33c2-108">A Get-AzSecuritySetting parancsmag biztonsági beállításokat kap az Azure Biztonsági központban.</span><span class="sxs-lookup"><span data-stu-id="c33c2-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="c33c2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c33c2-109">EXAMPLES</span></span>

### <span data-ttu-id="c33c2-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c33c2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="c33c2-111">MCAS-adatexport beállításokat ad meg</span><span class="sxs-lookup"><span data-stu-id="c33c2-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="c33c2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c33c2-112">PARAMETERS</span></span>

### <span data-ttu-id="c33c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33c2-113">-DefaultProfile</span></span>
<span data-ttu-id="c33c2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c33c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c33c2-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="c33c2-115">-SettingName</span></span>
<span data-ttu-id="c33c2-116">Beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="c33c2-116">Setting name.</span></span> <span data-ttu-id="c33c2-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="c33c2-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="c33c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33c2-118">CommonParameters</span></span>
<span data-ttu-id="c33c2-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c33c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33c2-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c33c2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33c2-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c33c2-121">INPUTS</span></span>

### <span data-ttu-id="c33c2-122">System.String</span><span class="sxs-lookup"><span data-stu-id="c33c2-122">System.String</span></span>

## <span data-ttu-id="c33c2-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c33c2-123">OUTPUTS</span></span>

### <span data-ttu-id="c33c2-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c33c2-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="c33c2-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="c33c2-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="c33c2-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c33c2-126">NOTES</span></span>

## <span data-ttu-id="c33c2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c33c2-127">RELATED LINKS</span></span>
