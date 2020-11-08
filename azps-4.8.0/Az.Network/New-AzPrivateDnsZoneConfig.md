---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025179"
---
# <span data-ttu-id="c104c-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="c104c-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="c104c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c104c-102">SYNOPSIS</span></span>
<span data-ttu-id="c104c-103">Létrehozza a DNS-zóna konfigurációját a privát DNS-zóna csoportban.</span><span class="sxs-lookup"><span data-stu-id="c104c-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="c104c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c104c-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c104c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c104c-105">DESCRIPTION</span></span>
<span data-ttu-id="c104c-106">A **New-AzPrivateDnsZoneConfig** parancsmaggal létrehozhatja az új DNS-zóna konfigurációs objektumát, amely a DNS Zone (DNS-zóna) csoportban lesz beállítva.</span><span class="sxs-lookup"><span data-stu-id="c104c-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="c104c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c104c-107">EXAMPLES</span></span>

### <span data-ttu-id="c104c-108">DNS-zóna konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="c104c-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="c104c-109">A fenti példa létrehozza a DNS-zónát, majd létrehozza a DNS-zóna konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c104c-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="c104c-110">`New-AzPrivateDnsZone` a parancsmagot az az. PrivateDns provededja.</span><span class="sxs-lookup"><span data-stu-id="c104c-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="c104c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c104c-111">PARAMETERS</span></span>

### <span data-ttu-id="c104c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c104c-112">-DefaultProfile</span></span>
<span data-ttu-id="c104c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c104c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c104c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c104c-114">-Name</span></span>
<span data-ttu-id="c104c-115">Az erőforrás-csoporton belüli egyedi erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c104c-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="c104c-116">Ezt a nevet az erőforrás eléréséhez használhatja.</span><span class="sxs-lookup"><span data-stu-id="c104c-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="c104c-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="c104c-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="c104c-118">A magánjellegű DNS-zóna erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c104c-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="c104c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c104c-119">CommonParameters</span></span>
<span data-ttu-id="c104c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c104c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c104c-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c104c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c104c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c104c-122">INPUTS</span></span>

### <span data-ttu-id="c104c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c104c-123">None</span></span>

## <span data-ttu-id="c104c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c104c-124">OUTPUTS</span></span>

### <span data-ttu-id="c104c-125">Microsoft. Azure. commands. Network. models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="c104c-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="c104c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c104c-126">NOTES</span></span>

## <span data-ttu-id="c104c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c104c-127">RELATED LINKS</span></span>
