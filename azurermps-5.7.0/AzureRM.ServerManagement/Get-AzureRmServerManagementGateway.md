---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9dc7e38cf169e79ec7dae279c6fa09f069b1ade7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492184"
---
# <span data-ttu-id="a42a2-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a42a2-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="a42a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a42a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a42a2-103">Egy vagy több kiszolgálói felügyeleti átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="a42a2-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a42a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a42a2-104">SYNTAX</span></span>

### <span data-ttu-id="a42a2-105">A paraméterek (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a42a2-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a42a2-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a42a2-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a42a2-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="a42a2-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a42a2-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="a42a2-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a42a2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a42a2-109">DESCRIPTION</span></span>
<span data-ttu-id="a42a2-110">A **Get-AzureRmServerManagementGateway** parancsmag egy vagy több Azure Server Management-átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="a42a2-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="a42a2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a42a2-111">EXAMPLES</span></span>

### <span data-ttu-id="a42a2-112">Példa 1: az összes átjáró beolvasása egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="a42a2-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="a42a2-113">Ez a parancs beilleszti az előfizetésben az összes kiszolgálóoldali kezelési átjárót.</span><span class="sxs-lookup"><span data-stu-id="a42a2-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="a42a2-114">2. példa: az átjárók beolvasása egy erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="a42a2-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="a42a2-115">Ez a parancs a Group001 nevű erőforráscsoport csoportjába tartozó összes Kiszolgálókezelő-átjárót beilleszti.</span><span class="sxs-lookup"><span data-stu-id="a42a2-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="a42a2-116">3. példa: az átjáró minden telepített példányának lekérése</span><span class="sxs-lookup"><span data-stu-id="a42a2-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="a42a2-117">Ez a parancs beolvassa a Gateway01 nevű Kiszolgálókezelő-átjáró minden előfordulását, amely a Group002 nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="a42a2-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="a42a2-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a42a2-118">PARAMETERS</span></span>

### <span data-ttu-id="a42a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a42a2-119">-DefaultProfile</span></span>
<span data-ttu-id="a42a2-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a42a2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a42a2-121">-Gateway</span><span class="sxs-lookup"><span data-stu-id="a42a2-121">-Gateway</span></span>
<span data-ttu-id="a42a2-122">Azt a átjárót adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="a42a2-122">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="a42a2-123">A parancsmag a *ResourceGroupName* és a *GatewayName* paramétert használja a megadott átjárón a művelet végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="a42a2-123">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="a42a2-124">Ha ezt a paramétert adja meg, ez a parancsmag az átjáró részletes állapotát fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="a42a2-124">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a42a2-125">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a42a2-125">-GatewayName</span></span>
<span data-ttu-id="a42a2-126">Annak a Kiszolgálókezelő-átjárónak a nevét adja meg, amelynek a parancsmagja a kaput kapja.</span><span class="sxs-lookup"><span data-stu-id="a42a2-126">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="a42a2-127">Ha a *GatewayName* paramétert adja meg, ez a parancsmag az átjáróban részletezett állapotot fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="a42a2-127">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a42a2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a42a2-128">-ResourceGroupName</span></span>
<span data-ttu-id="a42a2-129">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez ez a parancsmag átjárókat kap.</span><span class="sxs-lookup"><span data-stu-id="a42a2-129">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a42a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42a2-130">CommonParameters</span></span>
<span data-ttu-id="a42a2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a42a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42a2-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a42a2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42a2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a42a2-133">INPUTS</span></span>

### <span data-ttu-id="a42a2-134">Átjáró</span><span class="sxs-lookup"><span data-stu-id="a42a2-134">Gateway</span></span>
<span data-ttu-id="a42a2-135">Az "átjáró" paraméter elfogadja az "átjáró" típusú értéket a csővezetéken</span><span class="sxs-lookup"><span data-stu-id="a42a2-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="a42a2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a42a2-136">OUTPUTS</span></span>

### <span data-ttu-id="a42a2-137">Microsoft. Azure. Command. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="a42a2-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="a42a2-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a42a2-138">NOTES</span></span>
* <span data-ttu-id="a42a2-139">Ha ez a parancsmag paraméterek nélkül használatos, az előfizetéshez társított összes átjárót fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="a42a2-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="a42a2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a42a2-140">RELATED LINKS</span></span>

[<span data-ttu-id="a42a2-141">Új – AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a42a2-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="a42a2-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a42a2-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


