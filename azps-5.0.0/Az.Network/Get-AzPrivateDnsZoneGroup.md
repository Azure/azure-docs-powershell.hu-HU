---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194290"
---
# <span data-ttu-id="2ee9b-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="2ee9b-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="2ee9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ee9b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee9b-103">A privát DNS-zóna csoport lesz</span><span class="sxs-lookup"><span data-stu-id="2ee9b-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="2ee9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ee9b-104">SYNTAX</span></span>

### <span data-ttu-id="2ee9b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ee9b-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee9b-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="2ee9b-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee9b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ee9b-107">DESCRIPTION</span></span>
<span data-ttu-id="2ee9b-108">A **Get-AzPrivateDnsZoneGroup** parancsmag egy vagy több titkos DNS-zóna csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="2ee9b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2ee9b-109">EXAMPLES</span></span>

### <span data-ttu-id="2ee9b-110">Példa 1: személyes DNS-zóna csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="2ee9b-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="2ee9b-111">A fenti példa beolvassa a dnsgroup1 nevű privát DNS-zóna csoportot az erőforráscsoport RG csoportjában.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="2ee9b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ee9b-112">PARAMETERS</span></span>

### <span data-ttu-id="2ee9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee9b-113">-DefaultProfile</span></span>
<span data-ttu-id="2ee9b-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee9b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ee9b-115">-Name</span></span>
<span data-ttu-id="2ee9b-116">A privát DNS-zóna csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee9b-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="2ee9b-117">-PrivateEndpointName</span></span>
<span data-ttu-id="2ee9b-118">A privát végpont neve.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="2ee9b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee9b-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ee9b-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2ee9b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee9b-121">CommonParameters</span></span>
<span data-ttu-id="2ee9b-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ee9b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee9b-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee9b-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ee9b-124">INPUTS</span></span>

### <span data-ttu-id="2ee9b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee9b-125">System.String</span></span>

## <span data-ttu-id="2ee9b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ee9b-126">OUTPUTS</span></span>

### <span data-ttu-id="2ee9b-127">Microsoft. Azure. commands. Network. models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="2ee9b-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="2ee9b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ee9b-128">NOTES</span></span>

## <span data-ttu-id="2ee9b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ee9b-129">RELATED LINKS</span></span>
