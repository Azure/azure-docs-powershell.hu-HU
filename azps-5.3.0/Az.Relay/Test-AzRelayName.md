---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378012"
---
# <span data-ttu-id="549ec-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="549ec-101">Test-AzRelayName</span></span>

## <span data-ttu-id="549ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="549ec-102">SYNOPSIS</span></span>
<span data-ttu-id="549ec-103">A megadott Névtérnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="549ec-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="549ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="549ec-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="549ec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="549ec-105">DESCRIPTION</span></span>
<span data-ttu-id="549ec-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span><span class="sxs-lookup"><span data-stu-id="549ec-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="549ec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="549ec-107">EXAMPLES</span></span>

### <span data-ttu-id="549ec-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="549ec-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="549ec-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="549ec-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="549ec-110">3. példa</span><span class="sxs-lookup"><span data-stu-id="549ec-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="549ec-111">A névtérnév elérhetőségének állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="549ec-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="549ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="549ec-112">PARAMETERS</span></span>

### <span data-ttu-id="549ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549ec-113">-DefaultProfile</span></span>
<span data-ttu-id="549ec-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="549ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="549ec-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="549ec-115">-Namespace</span></span>
<span data-ttu-id="549ec-116">Relay Namespace Name (Továbbítás neve)</span><span class="sxs-lookup"><span data-stu-id="549ec-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="549ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549ec-117">CommonParameters</span></span>
<span data-ttu-id="549ec-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="549ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549ec-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="549ec-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549ec-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="549ec-120">INPUTS</span></span>

### <span data-ttu-id="549ec-121">System.String</span><span class="sxs-lookup"><span data-stu-id="549ec-121">System.String</span></span>

## <span data-ttu-id="549ec-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="549ec-122">OUTPUTS</span></span>

### <span data-ttu-id="549ec-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="549ec-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="549ec-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="549ec-124">NOTES</span></span>

## <span data-ttu-id="549ec-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="549ec-125">RELATED LINKS</span></span>
