---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 23a5fa01424d62796fec331213ffebb43121cec0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845426"
---
# <span data-ttu-id="040d8-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="040d8-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="040d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="040d8-102">SYNOPSIS</span></span>
<span data-ttu-id="040d8-103">Elérhető szolgáltatás-aliasok beszerzése a régióban.</span><span class="sxs-lookup"><span data-stu-id="040d8-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="040d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="040d8-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="040d8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="040d8-105">DESCRIPTION</span></span>
<span data-ttu-id="040d8-106">A **Get-AzAvailableServiceAlias** parancsmag lehetővé teszi, hogy az összes elérhető szolgáltatás-aliast visszanyerje a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="040d8-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="040d8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="040d8-107">EXAMPLES</span></span>

### <span data-ttu-id="040d8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="040d8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAliases -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="040d8-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="040d8-109">PARAMETERS</span></span>

### <span data-ttu-id="040d8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="040d8-110">-DefaultProfile</span></span>
<span data-ttu-id="040d8-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="040d8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="040d8-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="040d8-112">-Location</span></span>
<span data-ttu-id="040d8-113">A hely.</span><span class="sxs-lookup"><span data-stu-id="040d8-113">The location.</span></span>

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

### <span data-ttu-id="040d8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="040d8-114">CommonParameters</span></span>
<span data-ttu-id="040d8-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="040d8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="040d8-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="040d8-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="040d8-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="040d8-117">INPUTS</span></span>

### <span data-ttu-id="040d8-118">System. String</span><span class="sxs-lookup"><span data-stu-id="040d8-118">System.String</span></span>

## <span data-ttu-id="040d8-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="040d8-119">OUTPUTS</span></span>

### <span data-ttu-id="040d8-120">Microsoft. Azure. commands. Network. models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="040d8-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="040d8-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="040d8-121">NOTES</span></span>

## <span data-ttu-id="040d8-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="040d8-122">RELATED LINKS</span></span>
