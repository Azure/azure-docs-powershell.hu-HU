---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303917"
---
# <span data-ttu-id="df4ae-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="df4ae-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="df4ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="df4ae-103">Az Azure Advisor konfigurációjának beszerzése a megadott előfizetés vagy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="df4ae-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="df4ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df4ae-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df4ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df4ae-105">DESCRIPTION</span></span>
<span data-ttu-id="df4ae-106">Az előfizetéshez társított konfigurációk két típusa van:</span><span class="sxs-lookup"><span data-stu-id="df4ae-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="df4ae-107">Előfizetési szint beállítása: az előfizetéshez csak egy ilyen típusú konfiguráció lehet.</span><span class="sxs-lookup"><span data-stu-id="df4ae-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="df4ae-108">A LowCpuThreshold és a kihagyás az ilyen típusú konfiguráció egyetlen tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="df4ae-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="df4ae-109">ResourceGroup-szint beállítása: az előfizetések minden ResourceGroup csak egy konfiguráció lehet.</span><span class="sxs-lookup"><span data-stu-id="df4ae-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="df4ae-110">A kizárás csak az ilyen típusú konfiguráció egyetlen tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="df4ae-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="df4ae-111">Példák</span><span class="sxs-lookup"><span data-stu-id="df4ae-111">EXAMPLES</span></span>

### <span data-ttu-id="df4ae-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="df4ae-112">Example 1</span></span>
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
<span data-ttu-id="df4ae-113">Az Azure Advisor-konfiguráció (ok) listájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="df4ae-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="df4ae-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df4ae-114">PARAMETERS</span></span>

### <span data-ttu-id="df4ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4ae-115">-DefaultProfile</span></span>
<span data-ttu-id="df4ae-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df4ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="df4ae-118">A konfiguráció erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="df4ae-118">Resource Group name of the configuration</span></span>

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

### <span data-ttu-id="df4ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4ae-119">CommonParameters</span></span>
<span data-ttu-id="df4ae-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df4ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="df4ae-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4ae-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4ae-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df4ae-122">INPUTS</span></span>

### <span data-ttu-id="df4ae-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="df4ae-123">None</span></span>

## <span data-ttu-id="df4ae-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df4ae-124">OUTPUTS</span></span>

### <span data-ttu-id="df4ae-125">Microsoft. Azure. commands. Advisor. parancsmagok. models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="df4ae-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="df4ae-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df4ae-126">NOTES</span></span>

## <span data-ttu-id="df4ae-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df4ae-127">RELATED LINKS</span></span>
