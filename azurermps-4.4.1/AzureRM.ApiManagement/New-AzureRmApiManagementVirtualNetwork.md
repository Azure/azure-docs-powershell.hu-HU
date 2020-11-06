---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492614"
---
# <span data-ttu-id="ea049-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ea049-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="ea049-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea049-102">SYNOPSIS</span></span>
<span data-ttu-id="ea049-103">Létrehozza a PsApiManagementVirtualNetwork példányát.</span><span class="sxs-lookup"><span data-stu-id="ea049-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea049-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea049-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea049-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea049-105">DESCRIPTION</span></span>
<span data-ttu-id="ea049-106">A **New-AzureRmApiManagementVirtualNetwork** parancsmag a **PsApiManagementVirtualNetwork** példányának létrehozására szolgáló segítő parancs.</span><span class="sxs-lookup"><span data-stu-id="ea049-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="ea049-107">Ez a parancs a **set-AzureRMApiManagementVirtualNetworks** parancsmaggal használható.</span><span class="sxs-lookup"><span data-stu-id="ea049-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="ea049-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ea049-108">EXAMPLES</span></span>

### <span data-ttu-id="ea049-109">Példa 1: virtuális hálózat létrehozása</span><span class="sxs-lookup"><span data-stu-id="ea049-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="ea049-110">Ez a példa virtuális hálózatot hoz létre, majd felhívja a **set-AzureRmApiManagementVirtualNetworks** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ea049-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="ea049-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea049-111">PARAMETERS</span></span>

### <span data-ttu-id="ea049-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="ea049-112">-Location</span></span>
<span data-ttu-id="ea049-113">Annak a virtuális hálózatnak a helyét adja meg, amelyben ez a parancsmag létrehozta a példányt.</span><span class="sxs-lookup"><span data-stu-id="ea049-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="ea049-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ea049-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea049-115">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="ea049-115">North Central US</span></span>
- <span data-ttu-id="ea049-116">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="ea049-116">South Central US</span></span>
- <span data-ttu-id="ea049-117">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="ea049-117">Central US</span></span>
- <span data-ttu-id="ea049-118">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="ea049-118">West Europe</span></span>
- <span data-ttu-id="ea049-119">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="ea049-119">North Europe</span></span>
- <span data-ttu-id="ea049-120">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="ea049-120">West US</span></span>
- <span data-ttu-id="ea049-121">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="ea049-121">East US</span></span>
- <span data-ttu-id="ea049-122">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="ea049-122">East US 2</span></span>
- <span data-ttu-id="ea049-123">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="ea049-123">Japan East</span></span>
- <span data-ttu-id="ea049-124">Japán West</span><span class="sxs-lookup"><span data-stu-id="ea049-124">Japan West</span></span>
- <span data-ttu-id="ea049-125">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="ea049-125">Brazil South</span></span>
- <span data-ttu-id="ea049-126">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="ea049-126">Southeast Asia</span></span>
- <span data-ttu-id="ea049-127">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="ea049-127">East Asia</span></span>
- <span data-ttu-id="ea049-128">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="ea049-128">Australia East</span></span>
- <span data-ttu-id="ea049-129">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="ea049-129">Australia Southeast</span></span>

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

### <span data-ttu-id="ea049-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="ea049-130">-SubnetResourceId</span></span>
<span data-ttu-id="ea049-131">A virtuális hálózat alhálózati erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea049-131">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="ea049-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea049-132">-DefaultProfile</span></span>
<span data-ttu-id="ea049-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea049-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea049-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea049-134">CommonParameters</span></span>
<span data-ttu-id="ea049-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea049-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea049-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea049-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea049-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea049-137">INPUTS</span></span>

## <span data-ttu-id="ea049-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea049-138">OUTPUTS</span></span>

### <span data-ttu-id="ea049-139">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ea049-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="ea049-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea049-140">NOTES</span></span>

## <span data-ttu-id="ea049-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea049-141">RELATED LINKS</span></span>

