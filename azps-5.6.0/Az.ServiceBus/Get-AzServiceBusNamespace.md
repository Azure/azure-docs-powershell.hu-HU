---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: ef4d7ccf2f56d8a6d2a70fa4efb9468365cfcd32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939970"
---
# <span data-ttu-id="1090b-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1090b-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="1090b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1090b-102">SYNOPSIS</span></span>
<span data-ttu-id="1090b-103">Az erőforráscsoporton belül a szolgáltatás-busz névterének leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="1090b-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="1090b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1090b-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1090b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1090b-105">DESCRIPTION</span></span>
<span data-ttu-id="1090b-106">A **Get-AzServiceBusNamespace** parancsmag az erőforráscsoporton belül a szolgáltatásbusz névterének leírását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1090b-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="1090b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1090b-107">EXAMPLES</span></span>

### <span data-ttu-id="1090b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1090b-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="1090b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1090b-109">PARAMETERS</span></span>

### <span data-ttu-id="1090b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1090b-110">-DefaultProfile</span></span>
<span data-ttu-id="1090b-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1090b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1090b-112">-Name</span><span class="sxs-lookup"><span data-stu-id="1090b-112">-Name</span></span>
<span data-ttu-id="1090b-113">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="1090b-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1090b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1090b-114">-ResourceGroupName</span></span>
<span data-ttu-id="1090b-115">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1090b-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1090b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1090b-116">CommonParameters</span></span>
<span data-ttu-id="1090b-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1090b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1090b-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1090b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1090b-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1090b-119">INPUTS</span></span>

### <span data-ttu-id="1090b-120">System.String</span><span class="sxs-lookup"><span data-stu-id="1090b-120">System.String</span></span>

## <span data-ttu-id="1090b-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1090b-121">OUTPUTS</span></span>

### <span data-ttu-id="1090b-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1090b-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="1090b-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1090b-123">NOTES</span></span>

## <span data-ttu-id="1090b-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1090b-124">RELATED LINKS</span></span>
