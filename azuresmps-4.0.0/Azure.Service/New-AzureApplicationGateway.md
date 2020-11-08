---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016226"
---
# <span data-ttu-id="bf516-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf516-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="bf516-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf516-102">SYNOPSIS</span></span>
<span data-ttu-id="bf516-103">Egy Application Gatewayt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bf516-103">Creates an application gateway.</span></span>

## <span data-ttu-id="bf516-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf516-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf516-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf516-105">DESCRIPTION</span></span>
<span data-ttu-id="bf516-106">A **New-AzureApplicationGateway** parancsmag egy alkalmazás-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bf516-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="bf516-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf516-107">EXAMPLES</span></span>

### <span data-ttu-id="bf516-108">1. példa: alkalmazás-átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf516-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="bf516-109">Ez a parancs létrehoz egy ApplicationGateway06 nevű alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="bf516-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="bf516-110">A parancs a VirtualNetwork17-ban és a megadott alhálózatokban telepíti az átjárót.</span><span class="sxs-lookup"><span data-stu-id="bf516-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="bf516-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf516-111">PARAMETERS</span></span>

### <span data-ttu-id="bf516-112">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bf516-112">-Description</span></span>
<span data-ttu-id="bf516-113">Azt a leírást adja meg, amelyet a parancsmag az alkalmazás-átjáróhoz rendel.</span><span class="sxs-lookup"><span data-stu-id="bf516-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf516-114">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="bf516-114">-GatewaySize</span></span>
<span data-ttu-id="bf516-115">Azt adja meg, hogy a parancsmag milyen méretet rendel az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bf516-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="bf516-116">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bf516-116">Valid values are:</span></span>

- <span data-ttu-id="bf516-117">Kisvállalati</span><span class="sxs-lookup"><span data-stu-id="bf516-117">Small</span></span>
- <span data-ttu-id="bf516-118">Közepes</span><span class="sxs-lookup"><span data-stu-id="bf516-118">Medium</span></span>
- <span data-ttu-id="bf516-119">Nagy</span><span class="sxs-lookup"><span data-stu-id="bf516-119">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf516-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="bf516-120">-InstanceCount</span></span>
<span data-ttu-id="bf516-121">Azt adja meg, hogy a parancsmag hány példányt rendel az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bf516-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf516-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf516-122">-Name</span></span>
<span data-ttu-id="bf516-123">Az új alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf516-123">Specifies a name for the new application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf516-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf516-124">-Profile</span></span>
<span data-ttu-id="bf516-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="bf516-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf516-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="bf516-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf516-127">-Alhálózatok</span><span class="sxs-lookup"><span data-stu-id="bf516-127">-Subnets</span></span>
<span data-ttu-id="bf516-128">Itt adhatja meg azt az alhálózatokat, amelyben ez a parancsmag telepíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="bf516-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf516-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="bf516-129">-VnetName</span></span>
<span data-ttu-id="bf516-130">Annak a virtuális hálózatnak a meghatározása, amelyben ez a parancsmag telepíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="bf516-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf516-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf516-131">CommonParameters</span></span>
<span data-ttu-id="bf516-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf516-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf516-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf516-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf516-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf516-134">INPUTS</span></span>

### <span data-ttu-id="bf516-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bf516-135">System.String</span></span>

## <span data-ttu-id="bf516-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf516-136">OUTPUTS</span></span>

### <span data-ttu-id="bf516-137">Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bf516-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="bf516-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf516-138">NOTES</span></span>

## <span data-ttu-id="bf516-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf516-139">RELATED LINKS</span></span>

[<span data-ttu-id="bf516-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf516-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="bf516-141">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf516-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="bf516-142">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf516-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="bf516-143">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf516-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="bf516-144">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf516-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
