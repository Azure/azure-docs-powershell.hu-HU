---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185877"
---
# <span data-ttu-id="c0daf-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c0daf-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="c0daf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0daf-102">SYNOPSIS</span></span>
<span data-ttu-id="c0daf-103">Biztonsági beállítások kérése az Azure biztonsági központban</span><span class="sxs-lookup"><span data-stu-id="c0daf-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="c0daf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0daf-104">SYNTAX</span></span>

### <span data-ttu-id="c0daf-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0daf-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0daf-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c0daf-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0daf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0daf-107">DESCRIPTION</span></span>
<span data-ttu-id="c0daf-108">A Get-AzSecuritySetting parancsmag biztonsági beállításokat kap az Azure Security Centerben.</span><span class="sxs-lookup"><span data-stu-id="c0daf-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="c0daf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c0daf-109">EXAMPLES</span></span>

### <span data-ttu-id="c0daf-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c0daf-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="c0daf-111">MCAS-adatexportálási beállítás kérése</span><span class="sxs-lookup"><span data-stu-id="c0daf-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="c0daf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0daf-112">PARAMETERS</span></span>

### <span data-ttu-id="c0daf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0daf-113">-DefaultProfile</span></span>
<span data-ttu-id="c0daf-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0daf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0daf-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="c0daf-115">-SettingName</span></span>
<span data-ttu-id="c0daf-116">Beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="c0daf-116">Setting name.</span></span> <span data-ttu-id="c0daf-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="c0daf-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="c0daf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0daf-118">CommonParameters</span></span>
<span data-ttu-id="c0daf-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0daf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0daf-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0daf-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0daf-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0daf-121">INPUTS</span></span>

### <span data-ttu-id="c0daf-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c0daf-122">System.String</span></span>

## <span data-ttu-id="c0daf-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0daf-123">OUTPUTS</span></span>

### <span data-ttu-id="c0daf-124">Microsoft. Azure. Command. Security. models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c0daf-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="c0daf-125">Microsoft. Azure. Command. Security. models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="c0daf-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="c0daf-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0daf-126">NOTES</span></span>

## <span data-ttu-id="c0daf-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0daf-127">RELATED LINKS</span></span>
