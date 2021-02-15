---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151642"
---
# <span data-ttu-id="2e820-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="2e820-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="2e820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e820-102">SYNOPSIS</span></span>
<span data-ttu-id="2e820-103">Létrehozza a privát DNS-zónacsoport DNS-zónakonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2e820-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="2e820-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e820-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e820-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e820-105">DESCRIPTION</span></span>
<span data-ttu-id="2e820-106">A **New-AzPrivateDnsZoneConfig** parancsmaggal létrehozhat egy új DNS-zónakonfigurációs objektumot, amely a DNS-zónacsoportban lesz beállítva.</span><span class="sxs-lookup"><span data-stu-id="2e820-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="2e820-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e820-107">EXAMPLES</span></span>

### <span data-ttu-id="2e820-108">DNS-zónakonfigurációt hoz létre</span><span class="sxs-lookup"><span data-stu-id="2e820-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="2e820-109">A fenti példa létrehozza a DNS-zónát, majd létrehozza a DNS-zóna konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2e820-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="2e820-110">`New-AzPrivateDnsZone` A parancsmagot az Az.PrivateDns modul bizonyítja.</span><span class="sxs-lookup"><span data-stu-id="2e820-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="2e820-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e820-111">PARAMETERS</span></span>

### <span data-ttu-id="2e820-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e820-112">-DefaultProfile</span></span>
<span data-ttu-id="2e820-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e820-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e820-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2e820-114">-Name</span></span>
<span data-ttu-id="2e820-115">Az erőforráscsoporton belül egyedi erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2e820-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="2e820-116">Ez a név használható az erőforrás eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="2e820-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="2e820-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="2e820-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="2e820-118">A privát DNS-zóna erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e820-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="2e820-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e820-119">CommonParameters</span></span>
<span data-ttu-id="2e820-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e820-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e820-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e820-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e820-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e820-122">INPUTS</span></span>

### <span data-ttu-id="2e820-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="2e820-123">None</span></span>

## <span data-ttu-id="2e820-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e820-124">OUTPUTS</span></span>

### <span data-ttu-id="2e820-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="2e820-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="2e820-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e820-126">NOTES</span></span>

## <span data-ttu-id="2e820-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e820-127">RELATED LINKS</span></span>
