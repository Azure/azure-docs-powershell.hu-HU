---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 4eb210380feaaf101bad45b4bd0b4df26533f9e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940242"
---
# <span data-ttu-id="ff885-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="ff885-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="ff885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff885-102">SYNOPSIS</span></span>
<span data-ttu-id="ff885-103">Elérhető szolgáltatási aliasok lekérhetők a régióban.</span><span class="sxs-lookup"><span data-stu-id="ff885-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="ff885-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ff885-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff885-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ff885-105">DESCRIPTION</span></span>
<span data-ttu-id="ff885-106">A **Get-AzAvailableServiceAlias** parancsmag lehetővé teszi az alhálózat összes rendelkezésre álló szolgáltatásaliasának beolvasását a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="ff885-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="ff885-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ff885-107">EXAMPLES</span></span>

### <span data-ttu-id="ff885-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ff885-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="ff885-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff885-109">PARAMETERS</span></span>

### <span data-ttu-id="ff885-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff885-110">-DefaultProfile</span></span>
<span data-ttu-id="ff885-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff885-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff885-112">-Location</span><span class="sxs-lookup"><span data-stu-id="ff885-112">-Location</span></span>
<span data-ttu-id="ff885-113">A hely.</span><span class="sxs-lookup"><span data-stu-id="ff885-113">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff885-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff885-114">CommonParameters</span></span>
<span data-ttu-id="ff885-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff885-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff885-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff885-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff885-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff885-117">INPUTS</span></span>

### <span data-ttu-id="ff885-118">System.String</span><span class="sxs-lookup"><span data-stu-id="ff885-118">System.String</span></span>

## <span data-ttu-id="ff885-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff885-119">OUTPUTS</span></span>

### <span data-ttu-id="ff885-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="ff885-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="ff885-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ff885-121">NOTES</span></span>

## <span data-ttu-id="ff885-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff885-122">RELATED LINKS</span></span>
