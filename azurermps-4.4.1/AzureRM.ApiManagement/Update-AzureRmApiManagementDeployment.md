---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492588"
---
# <span data-ttu-id="c9dca-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c9dca-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="c9dca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9dca-102">SYNOPSIS</span></span>
<span data-ttu-id="c9dca-103">Frissíti az API-kezelési szolgáltatás telepítését.</span><span class="sxs-lookup"><span data-stu-id="c9dca-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9dca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9dca-104">SYNTAX</span></span>

### <span data-ttu-id="c9dca-105">Adott API-kezelési szolgáltatás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9dca-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9dca-106">Frissítés a PsApiManagement-példányról</span><span class="sxs-lookup"><span data-stu-id="c9dca-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9dca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9dca-107">DESCRIPTION</span></span>
<span data-ttu-id="c9dca-108">Az **Update-AzureRmApiManagementDeployment** parancsmag FRISSÍTI az API-kezelési szolgáltatás aktuális telepített példányait.</span><span class="sxs-lookup"><span data-stu-id="c9dca-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="c9dca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c9dca-109">EXAMPLES</span></span>

### <span data-ttu-id="c9dca-110">Példa 1: egy ApiManagement példány telepített példányának frissítése</span><span class="sxs-lookup"><span data-stu-id="c9dca-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="c9dca-111">Ez a parancs frissíti az API-kezelési példányok három egységnyi kapacitású szabványba való bevezetését.</span><span class="sxs-lookup"><span data-stu-id="c9dca-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="c9dca-112">2. példa: ApiManagement-példány beszerzése és átméretezése</span><span class="sxs-lookup"><span data-stu-id="c9dca-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="c9dca-113">Ebben a példában egy API-kezelési példány válik, és öt prémium egységre méretezi, majd egy további három egységet ad hozzá a prémium régióhoz.</span><span class="sxs-lookup"><span data-stu-id="c9dca-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="c9dca-114">3. példa: a frissítés telepítése (külső VNET)</span><span class="sxs-lookup"><span data-stu-id="c9dca-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="c9dca-115">Ez a parancs frissíti egy meglévő API-kezelési telepítőt, és csatlakozik egy külső *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="c9dca-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="c9dca-116">4. példa: a frissítés telepítése (belső VNET)</span><span class="sxs-lookup"><span data-stu-id="c9dca-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="c9dca-117">Ez a parancs frissíti egy meglévő API-kezelési üzembe állítást, és csatlakozik egy belső *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="c9dca-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="c9dca-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9dca-118">PARAMETERS</span></span>

### <span data-ttu-id="c9dca-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="c9dca-119">-AdditionalRegions</span></span>
<span data-ttu-id="c9dca-120">Az Azure API-menedzsment további központi terjesztési területeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9dca-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9dca-121">-ApiManagement</span></span>
<span data-ttu-id="c9dca-122">Azt a **PsApiManagement** -példányt adja meg, amelyből beolvassa a telepítő konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c9dca-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="c9dca-123">Akkor használja ezt a paramétert, ha a példány már rendelkezik az összes szükséges módosítással.</span><span class="sxs-lookup"><span data-stu-id="c9dca-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-124">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="c9dca-124">-Capacity</span></span>
<span data-ttu-id="c9dca-125">Itt adhatja meg az Azure API-alapú központi telepítő terület SKU-kapacitását.</span><span class="sxs-lookup"><span data-stu-id="c9dca-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="c9dca-126">-Location</span></span>
<span data-ttu-id="c9dca-127">A fő API-kezelés központi központi telepítéséhez használható terület helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9dca-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="c9dca-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c9dca-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9dca-129">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="c9dca-129">North Central US</span></span>
- <span data-ttu-id="c9dca-130">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="c9dca-130">South Central US</span></span>
- <span data-ttu-id="c9dca-131">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="c9dca-131">Central US</span></span>
- <span data-ttu-id="c9dca-132">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="c9dca-132">West Europe</span></span>
- <span data-ttu-id="c9dca-133">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="c9dca-133">North Europe</span></span>
- <span data-ttu-id="c9dca-134">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="c9dca-134">West US</span></span>
- <span data-ttu-id="c9dca-135">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="c9dca-135">East US</span></span>
- <span data-ttu-id="c9dca-136">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="c9dca-136">East US 2</span></span>
- <span data-ttu-id="c9dca-137">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="c9dca-137">Japan East</span></span>
- <span data-ttu-id="c9dca-138">Japán West</span><span class="sxs-lookup"><span data-stu-id="c9dca-138">Japan West</span></span>
- <span data-ttu-id="c9dca-139">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="c9dca-139">Brazil South</span></span>
- <span data-ttu-id="c9dca-140">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="c9dca-140">Southeast Asia</span></span>
- <span data-ttu-id="c9dca-141">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="c9dca-141">East Asia</span></span>
- <span data-ttu-id="c9dca-142">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="c9dca-142">Australia East</span></span>
- <span data-ttu-id="c9dca-143">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="c9dca-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9dca-144">-Name</span></span>
<span data-ttu-id="c9dca-145">A parancsmag által frissített API-kezelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9dca-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9dca-146">-PassThru</span></span>
<span data-ttu-id="c9dca-147">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c9dca-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c9dca-148">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c9dca-148">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9dca-149">-ResourceGroupName</span></span>
<span data-ttu-id="c9dca-150">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="c9dca-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="c9dca-151">-Sku</span></span>
<span data-ttu-id="c9dca-152">Itt adhatja meg az Azure API-kezelés központi központi telepítéséhez tartozó terület rétegét.</span><span class="sxs-lookup"><span data-stu-id="c9dca-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="c9dca-153">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c9dca-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9dca-154">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="c9dca-154">Developer</span></span>
- <span data-ttu-id="c9dca-155">Standard</span><span class="sxs-lookup"><span data-stu-id="c9dca-155">Standard</span></span>
- <span data-ttu-id="c9dca-156">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="c9dca-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c9dca-157">-VirtualNetwork</span></span>
<span data-ttu-id="c9dca-158">A fő Azure API-kezelési terület virtuális hálózati konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9dca-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="c9dca-159">-VpnType</span></span>
<span data-ttu-id="c9dca-160">Az API-kezelés központi telepítését megadó virtuális hálózati típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9dca-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="c9dca-161">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c9dca-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9dca-162">Nincs.</span><span class="sxs-lookup"><span data-stu-id="c9dca-162">None.</span></span>
<span data-ttu-id="c9dca-163">Az API-kezelés bevezetése nem része bármely virtuális hálózatnak.</span><span class="sxs-lookup"><span data-stu-id="c9dca-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="c9dca-164">Ez az alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="c9dca-164">This is the default value.</span></span> 
- <span data-ttu-id="c9dca-165">Külső.</span><span class="sxs-lookup"><span data-stu-id="c9dca-165">External.</span></span>
<span data-ttu-id="c9dca-166">Az API-kezelés bevezetésének külső virtuális címe van.</span><span class="sxs-lookup"><span data-stu-id="c9dca-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="c9dca-167">Belső.</span><span class="sxs-lookup"><span data-stu-id="c9dca-167">Internal.</span></span>
<span data-ttu-id="c9dca-168">Az API-kezelés központi központi elérési környezete intranetes virtuális címet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c9dca-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dca-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9dca-169">-DefaultProfile</span></span>
<span data-ttu-id="c9dca-170">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9dca-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9dca-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9dca-171">CommonParameters</span></span>
<span data-ttu-id="c9dca-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9dca-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9dca-173">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9dca-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9dca-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9dca-174">INPUTS</span></span>

### <span data-ttu-id="c9dca-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9dca-175">PsApiManagement</span></span>
<span data-ttu-id="c9dca-176">A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c9dca-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="c9dca-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9dca-177">OUTPUTS</span></span>

### <span data-ttu-id="c9dca-178">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9dca-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c9dca-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9dca-179">NOTES</span></span>

## <span data-ttu-id="c9dca-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9dca-180">RELATED LINKS</span></span>

[<span data-ttu-id="c9dca-181">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9dca-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


