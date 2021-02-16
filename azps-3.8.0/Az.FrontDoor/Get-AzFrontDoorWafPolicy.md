---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: daf4631041093b10a1bf712649de8b5c3ad3b6d9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404020"
---
# <span data-ttu-id="0debf-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="0debf-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="0debf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0debf-102">SYNOPSIS</span></span>
<span data-ttu-id="0debf-103">A waf-szabályzat lekérte</span><span class="sxs-lookup"><span data-stu-id="0debf-103">Get WAF policy</span></span>

## <span data-ttu-id="0debf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0debf-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0debf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0debf-105">DESCRIPTION</span></span>
<span data-ttu-id="0debf-106">A **Get-AzFrontDoorWafPolicy** parancsmagGet a WAF-házirendet az aktuális előfizetés alatti erőforráscsoportba kapja</span><span class="sxs-lookup"><span data-stu-id="0debf-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="0debf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0debf-107">EXAMPLES</span></span>

### <span data-ttu-id="0debf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0debf-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="0debf-109">A waf-házirendek $policyName a $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0debf-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="0debf-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0debf-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="0debf-111">A WaF-házirendek $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0debf-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="0debf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0debf-112">PARAMETERS</span></span>

### <span data-ttu-id="0debf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0debf-113">-DefaultProfile</span></span>
<span data-ttu-id="0debf-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0debf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0debf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0debf-115">-Name</span></span>
<span data-ttu-id="0debf-116">FireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="0debf-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0debf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0debf-117">-ResourceGroupName</span></span>
<span data-ttu-id="0debf-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0debf-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0debf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0debf-119">CommonParameters</span></span>
<span data-ttu-id="0debf-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0debf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0debf-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0debf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0debf-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0debf-122">INPUTS</span></span>

### <span data-ttu-id="0debf-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="0debf-123">None</span></span>

## <span data-ttu-id="0debf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0debf-124">OUTPUTS</span></span>

### <span data-ttu-id="0debf-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0debf-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="0debf-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0debf-126">NOTES</span></span>

## <span data-ttu-id="0debf-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0debf-127">RELATED LINKS</span></span>

<span data-ttu-id="0debf-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="0debf-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
