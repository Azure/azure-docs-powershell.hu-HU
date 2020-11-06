---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 2bcfac139d38f0b6f7d621a7761ce01d1d3f2f45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496868"
---
# <span data-ttu-id="35d41-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="35d41-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="35d41-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35d41-102">SYNOPSIS</span></span>
<span data-ttu-id="35d41-103">Kiszolgáló-kezelési átjáró eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="35d41-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35d41-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35d41-104">SYNTAX</span></span>

### <span data-ttu-id="35d41-105">ByName</span><span class="sxs-lookup"><span data-stu-id="35d41-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35d41-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="35d41-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35d41-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="35d41-107">DESCRIPTION</span></span>
<span data-ttu-id="35d41-108">A **Remove-AzureRmServerManagementGateway** parancsmag eltávolítja az Azure Server Management átjárót.</span><span class="sxs-lookup"><span data-stu-id="35d41-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="35d41-109">Példák</span><span class="sxs-lookup"><span data-stu-id="35d41-109">EXAMPLES</span></span>

## <span data-ttu-id="35d41-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35d41-110">PARAMETERS</span></span>

### <span data-ttu-id="35d41-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="35d41-111">-Gateway</span></span>
<span data-ttu-id="35d41-112">A parancsmag által eltávolított átjárót adja meg.</span><span class="sxs-lookup"><span data-stu-id="35d41-112">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="35d41-113">Ezt a paramétert a *ResourceGroupName* és a *GatewayName* paraméterek helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="35d41-113">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35d41-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="35d41-114">-GatewayName</span></span>
<span data-ttu-id="35d41-115">Annak az átjárónak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="35d41-115">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35d41-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d41-116">-ResourceGroupName</span></span>
<span data-ttu-id="35d41-117">Annak az erőforrás-csoportnak a nevét adja meg, amelybe az átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="35d41-117">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35d41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d41-118">-DefaultProfile</span></span>
<span data-ttu-id="35d41-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35d41-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d41-120">CommonParameters</span></span>
<span data-ttu-id="35d41-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35d41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d41-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d41-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d41-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35d41-123">INPUTS</span></span>

### <span data-ttu-id="35d41-124">Átjáró</span><span class="sxs-lookup"><span data-stu-id="35d41-124">Gateway</span></span>
<span data-ttu-id="35d41-125">Az "átjáró" paraméter elfogadja az "átjáró" típusú értéket a csővezetéken</span><span class="sxs-lookup"><span data-stu-id="35d41-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="35d41-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35d41-126">OUTPUTS</span></span>

## <span data-ttu-id="35d41-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35d41-127">NOTES</span></span>
* <span data-ttu-id="35d41-128">Az átjáró összes csomópontját el kell távolítani, mielőtt a parancsmagot használja. egyéb esetekben ez a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="35d41-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="35d41-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35d41-129">RELATED LINKS</span></span>

[<span data-ttu-id="35d41-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="35d41-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="35d41-131">Új – AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="35d41-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


