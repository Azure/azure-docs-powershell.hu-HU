---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165994"
---
# <span data-ttu-id="e205d-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="e205d-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="e205d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e205d-102">SYNOPSIS</span></span>
<span data-ttu-id="e205d-103">Leírást ad a Továbbító névterében megadott HybridConnectionhoz.</span><span class="sxs-lookup"><span data-stu-id="e205d-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="e205d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e205d-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e205d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e205d-105">DESCRIPTION</span></span>
<span data-ttu-id="e205d-106">A **Get-AzRelayHybridConnection** parancsmag a Továbbítás névterében található megadott HybridConnection parancsmag leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="e205d-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="e205d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e205d-107">EXAMPLES</span></span>

### <span data-ttu-id="e205d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e205d-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="e205d-109">A HybridConnection leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e205d-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="e205d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e205d-110">PARAMETERS</span></span>

### <span data-ttu-id="e205d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e205d-111">-DefaultProfile</span></span>
<span data-ttu-id="e205d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e205d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e205d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e205d-113">-Name</span></span>
<span data-ttu-id="e205d-114">HybridConnections Name.</span><span class="sxs-lookup"><span data-stu-id="e205d-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e205d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e205d-115">-Namespace</span></span>
<span data-ttu-id="e205d-116">Namespace Name (Név)</span><span class="sxs-lookup"><span data-stu-id="e205d-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e205d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e205d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e205d-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e205d-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e205d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e205d-119">CommonParameters</span></span>
<span data-ttu-id="e205d-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e205d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e205d-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e205d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e205d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e205d-122">INPUTS</span></span>

### <span data-ttu-id="e205d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e205d-123">System.String</span></span>

## <span data-ttu-id="e205d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e205d-124">OUTPUTS</span></span>

### <span data-ttu-id="e205d-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="e205d-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="e205d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e205d-126">NOTES</span></span>

## <span data-ttu-id="e205d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e205d-127">RELATED LINKS</span></span>
