---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469153"
---
# <span data-ttu-id="ad593-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad593-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="ad593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad593-102">SYNOPSIS</span></span>
<span data-ttu-id="ad593-103">Szerezze be az Adott előfizetéshez vagy erőforráscsoporthoz az Azure Advisor-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="ad593-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="ad593-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad593-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad593-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad593-105">DESCRIPTION</span></span>
<span data-ttu-id="ad593-106">Az előfizetéshez társított konfigurációknak két típusa van:</span><span class="sxs-lookup"><span data-stu-id="ad593-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="ad593-107">Előfizetési szintű konfiguráció: Egy előfizetéshez csak egy ilyen típusú konfiguráció lehet.</span><span class="sxs-lookup"><span data-stu-id="ad593-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="ad593-108">Az ilyen típusú konfigurációk egyetlen tulajdonsága a LowCpuThreshold és az Exclude.</span><span class="sxs-lookup"><span data-stu-id="ad593-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="ad593-109">Erőforráscsoport szintű konfiguráció: Egy előfizetésben minden Erőforráscsoporthoz csak egy konfiguráció lehet.</span><span class="sxs-lookup"><span data-stu-id="ad593-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="ad593-110">Az ilyen típusú konfigurációnak az Kizárás az egyetlen tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="ad593-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="ad593-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad593-111">EXAMPLES</span></span>

### <span data-ttu-id="ad593-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="ad593-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="ad593-113">Beolvassa az Azure Advisor configuration(k) listáját.</span><span class="sxs-lookup"><span data-stu-id="ad593-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="ad593-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad593-114">PARAMETERS</span></span>

### <span data-ttu-id="ad593-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad593-115">-DefaultProfile</span></span>
<span data-ttu-id="ad593-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad593-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad593-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad593-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad593-118">A konfiguráció erőforráscsoportjának neve</span><span class="sxs-lookup"><span data-stu-id="ad593-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad593-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad593-119">CommonParameters</span></span>
<span data-ttu-id="ad593-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad593-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ad593-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad593-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad593-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad593-122">INPUTS</span></span>

### <span data-ttu-id="ad593-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="ad593-123">None</span></span>

## <span data-ttu-id="ad593-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad593-124">OUTPUTS</span></span>

### <span data-ttu-id="ad593-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="ad593-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="ad593-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad593-126">NOTES</span></span>

## <span data-ttu-id="ad593-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad593-127">RELATED LINKS</span></span>
