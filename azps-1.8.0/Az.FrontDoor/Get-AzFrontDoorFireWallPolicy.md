---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 5933d860ca2badce2d9576409dd1553153bb1e84
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401504"
---
# <span data-ttu-id="f65a8-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="f65a8-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="f65a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f65a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f65a8-103">A waf-szabályzat lekérte</span><span class="sxs-lookup"><span data-stu-id="f65a8-103">Get WAF policy</span></span>

## <span data-ttu-id="f65a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f65a8-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f65a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f65a8-105">DESCRIPTION</span></span>
<span data-ttu-id="f65a8-106">A **Get-AzFrontDoorFireWallPolicy** parancsmagGet a WAF-házirendet az aktuális előfizetés alatti erőforráscsoportba kapja</span><span class="sxs-lookup"><span data-stu-id="f65a8-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="f65a8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f65a8-107">EXAMPLES</span></span>

### <span data-ttu-id="f65a8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f65a8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="f65a8-109">Az új $policyName waf$resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65a8-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="f65a8-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="f65a8-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="f65a8-111">A WaF-házirendek $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65a8-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="f65a8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f65a8-112">PARAMETERS</span></span>

### <span data-ttu-id="f65a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65a8-113">-DefaultProfile</span></span>
<span data-ttu-id="f65a8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f65a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f65a8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f65a8-115">-Name</span></span>
<span data-ttu-id="f65a8-116">FireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="f65a8-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="f65a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="f65a8-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f65a8-118">The resource group name.</span></span>

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

### <span data-ttu-id="f65a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65a8-119">CommonParameters</span></span>
<span data-ttu-id="f65a8-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f65a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65a8-121">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f65a8-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65a8-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f65a8-122">INPUTS</span></span>

### <span data-ttu-id="f65a8-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="f65a8-123">None</span></span>

## <span data-ttu-id="f65a8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f65a8-124">OUTPUTS</span></span>

### <span data-ttu-id="f65a8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f65a8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="f65a8-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f65a8-126">NOTES</span></span>

## <span data-ttu-id="f65a8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f65a8-127">RELATED LINKS</span></span>

<span data-ttu-id="f65a8-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f65a8-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
