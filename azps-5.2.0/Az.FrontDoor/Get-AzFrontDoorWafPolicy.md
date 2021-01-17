---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350237"
---
# <span data-ttu-id="fd84b-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="fd84b-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="fd84b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd84b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd84b-103">A waf-szabályzat lekérte</span><span class="sxs-lookup"><span data-stu-id="fd84b-103">Get WAF policy</span></span>

## <span data-ttu-id="fd84b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd84b-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd84b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd84b-105">DESCRIPTION</span></span>
<span data-ttu-id="fd84b-106">A **Get-AzFrontDoorWafPolicy** parancsmagGet a WAF-házirendet az aktuális előfizetés alatti erőforráscsoportba kapja</span><span class="sxs-lookup"><span data-stu-id="fd84b-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="fd84b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd84b-107">EXAMPLES</span></span>

### <span data-ttu-id="fd84b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd84b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="fd84b-109">Az új $policyName waf$resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd84b-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="fd84b-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd84b-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="fd84b-111">A WaF-házirendek $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd84b-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="fd84b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd84b-112">PARAMETERS</span></span>

### <span data-ttu-id="fd84b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd84b-113">-DefaultProfile</span></span>
<span data-ttu-id="fd84b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd84b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd84b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fd84b-115">-Name</span></span>
<span data-ttu-id="fd84b-116">FireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="fd84b-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="fd84b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd84b-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd84b-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd84b-118">The resource group name.</span></span>

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

### <span data-ttu-id="fd84b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd84b-119">CommonParameters</span></span>
<span data-ttu-id="fd84b-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd84b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd84b-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd84b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd84b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd84b-122">INPUTS</span></span>

### <span data-ttu-id="fd84b-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="fd84b-123">None</span></span>

## <span data-ttu-id="fd84b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd84b-124">OUTPUTS</span></span>

### <span data-ttu-id="fd84b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="fd84b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="fd84b-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd84b-126">NOTES</span></span>

## <span data-ttu-id="fd84b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd84b-127">RELATED LINKS</span></span>

<span data-ttu-id="fd84b-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="fd84b-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
