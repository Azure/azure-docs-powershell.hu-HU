---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496872"
---
# <span data-ttu-id="a0d44-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a0d44-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="a0d44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0d44-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d44-103">Kiszolgáló-kezelési átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="a0d44-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0d44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0d44-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0d44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0d44-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d44-106">A **New-AzureRmServerManagementGateway** parancsmag egy Azure Server Management átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a0d44-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="a0d44-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0d44-107">EXAMPLES</span></span>

## <span data-ttu-id="a0d44-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0d44-108">PARAMETERS</span></span>

### <span data-ttu-id="a0d44-109">-Autoupgrade</span><span class="sxs-lookup"><span data-stu-id="a0d44-109">-AutoUpgrade</span></span>
<span data-ttu-id="a0d44-110">Jelzi, hogy az átjáró automatikusan frissíti magát új verzió megjelenésekor.</span><span class="sxs-lookup"><span data-stu-id="a0d44-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d44-111">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a0d44-111">-GatewayName</span></span>
<span data-ttu-id="a0d44-112">A parancsmag által létrehozott átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0d44-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a0d44-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="a0d44-113">-Location</span></span>
<span data-ttu-id="a0d44-114">Az átjáró létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0d44-114">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d44-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d44-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0d44-116">Annak az erőforrás csoportnak a nevét adja meg, amelyben ez a parancsmag létrehozta az átjárót.</span><span class="sxs-lookup"><span data-stu-id="a0d44-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="a0d44-117">-Címkék</span><span class="sxs-lookup"><span data-stu-id="a0d44-117">-Tags</span></span>
<span data-ttu-id="a0d44-118">A címkéket kulcs-érték párokként adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0d44-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="a0d44-119">A címkéket használhat más Azure-erőforrásokból származó átjárók kiszűrésére is.</span><span class="sxs-lookup"><span data-stu-id="a0d44-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d44-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d44-120">-DefaultProfile</span></span>
<span data-ttu-id="a0d44-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0d44-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0d44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d44-122">CommonParameters</span></span>
<span data-ttu-id="a0d44-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0d44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d44-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d44-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d44-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0d44-125">INPUTS</span></span>

## <span data-ttu-id="a0d44-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0d44-126">OUTPUTS</span></span>

### <span data-ttu-id="a0d44-127">Microsoft. Azure. Command. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="a0d44-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="a0d44-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0d44-128">NOTES</span></span>

## <span data-ttu-id="a0d44-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0d44-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0d44-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a0d44-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="a0d44-131">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a0d44-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


