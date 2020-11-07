---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672358"
---
# <span data-ttu-id="6fbe8-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6fbe8-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="6fbe8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fbe8-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbe8-103">Kiszolgáló-kezelési átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="6fbe8-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fbe8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fbe8-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fbe8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fbe8-105">DESCRIPTION</span></span>
<span data-ttu-id="6fbe8-106">A **New-AzureRmServerManagementGateway** parancsmag egy Azure Server Management átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6fbe8-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="6fbe8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6fbe8-107">EXAMPLES</span></span>

## <span data-ttu-id="6fbe8-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fbe8-108">PARAMETERS</span></span>

### <span data-ttu-id="6fbe8-109">-Autoupgrade</span><span class="sxs-lookup"><span data-stu-id="6fbe8-109">-AutoUpgrade</span></span>
<span data-ttu-id="6fbe8-110">Jelzi, hogy az átjáró automatikusan frissíti magát új verzió megjelenésekor.</span><span class="sxs-lookup"><span data-stu-id="6fbe8-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbe8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbe8-111">-DefaultProfile</span></span>
<span data-ttu-id="6fbe8-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fbe8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fbe8-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="6fbe8-113">-GatewayName</span></span>
<span data-ttu-id="6fbe8-114">A parancsmag által létrehozott átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fbe8-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbe8-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="6fbe8-115">-Location</span></span>
<span data-ttu-id="6fbe8-116">Az átjáró létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fbe8-116">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbe8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbe8-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fbe8-118">Annak az erőforrás csoportnak a nevét adja meg, amelyben ez a parancsmag létrehozta az átjárót.</span><span class="sxs-lookup"><span data-stu-id="6fbe8-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbe8-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="6fbe8-119">-Tag</span></span>
<span data-ttu-id="6fbe8-120">Az átjáróhoz társított kulcs/érték párok.</span><span class="sxs-lookup"><span data-stu-id="6fbe8-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbe8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbe8-121">CommonParameters</span></span>
<span data-ttu-id="6fbe8-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fbe8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbe8-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbe8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbe8-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fbe8-124">INPUTS</span></span>

### <span data-ttu-id="6fbe8-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="6fbe8-125">None</span></span>
<span data-ttu-id="6fbe8-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6fbe8-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6fbe8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fbe8-127">OUTPUTS</span></span>

### <span data-ttu-id="6fbe8-128">Microsoft. Azure. Command. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="6fbe8-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="6fbe8-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fbe8-129">NOTES</span></span>

## <span data-ttu-id="6fbe8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fbe8-130">RELATED LINKS</span></span>

[<span data-ttu-id="6fbe8-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6fbe8-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="6fbe8-132">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6fbe8-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


