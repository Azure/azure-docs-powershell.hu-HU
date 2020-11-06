---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492898"
---
# <span data-ttu-id="73573-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="73573-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="73573-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73573-102">SYNOPSIS</span></span>
<span data-ttu-id="73573-103">Frissíti az API-kezelési szolgáltatás telepítését.</span><span class="sxs-lookup"><span data-stu-id="73573-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73573-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73573-104">SYNTAX</span></span>

### <span data-ttu-id="73573-105">UpdateSpecificService (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73573-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73573-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="73573-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73573-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="73573-107">DESCRIPTION</span></span>
<span data-ttu-id="73573-108">Az **Update-AzureRmApiManagementDeployment** parancsmag FRISSÍTI az API-kezelési szolgáltatás aktuális telepített példányait.</span><span class="sxs-lookup"><span data-stu-id="73573-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="73573-109">Példák</span><span class="sxs-lookup"><span data-stu-id="73573-109">EXAMPLES</span></span>

### <span data-ttu-id="73573-110">Példa 1: egy ApiManagement példány telepített példányának frissítése</span><span class="sxs-lookup"><span data-stu-id="73573-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="73573-111">Ez a parancs frissíti az API-kezelési példányok három egységnyi kapacitású szabványba való bevezetését.</span><span class="sxs-lookup"><span data-stu-id="73573-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="73573-112">2. példa: ApiManagement-példány beszerzése és átméretezése</span><span class="sxs-lookup"><span data-stu-id="73573-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="73573-113">Ebben a példában egy API-kezelési példány válik, és öt prémium egységre méretezi, majd egy további három egységet ad hozzá a prémium régióhoz.</span><span class="sxs-lookup"><span data-stu-id="73573-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="73573-114">3. példa: a frissítés telepítése (külső VNET)</span><span class="sxs-lookup"><span data-stu-id="73573-114">Example 3: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="73573-115">Ez a parancs frissíti egy meglévő API-kezelési telepítőt, és csatlakozik egy külső *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="73573-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="73573-116">4. példa: a frissítés telepítése (belső VNET)</span><span class="sxs-lookup"><span data-stu-id="73573-116">Example 4: Update deployment (internal VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="73573-117">Ez a parancs frissíti egy meglévő API-kezelési üzembe állítást, és csatlakozik egy belső *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="73573-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="73573-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73573-118">PARAMETERS</span></span>

### <span data-ttu-id="73573-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="73573-119">-AdditionalRegions</span></span>
<span data-ttu-id="73573-120">Az Azure API-menedzsment további központi terjesztési területeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="73573-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73573-121">-ApiManagement</span></span>
<span data-ttu-id="73573-122">Azt a **PsApiManagement** -példányt adja meg, amelyből beolvassa a telepítő konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="73573-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="73573-123">Akkor használja ezt a paramétert, ha a példány már rendelkezik az összes szükséges módosítással.</span><span class="sxs-lookup"><span data-stu-id="73573-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-124">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="73573-124">-Capacity</span></span>
<span data-ttu-id="73573-125">Itt adhatja meg az Azure API-alapú központi telepítő terület SKU-kapacitását.</span><span class="sxs-lookup"><span data-stu-id="73573-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73573-126">-DefaultProfile</span></span>
<span data-ttu-id="73573-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73573-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73573-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="73573-128">-Location</span></span>
<span data-ttu-id="73573-129">A fő API-kezelés központi központi telepítéséhez használható terület helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73573-129">Specifies the location of the master API Management deployment region.</span></span>
<span data-ttu-id="73573-130">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="73573-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73573-131">-Name</span></span>
<span data-ttu-id="73573-132">A parancsmag által frissített API-kezelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73573-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73573-133">-PassThru</span></span>
<span data-ttu-id="73573-134">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="73573-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="73573-135">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="73573-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="73573-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73573-136">-ResourceGroupName</span></span>
<span data-ttu-id="73573-137">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="73573-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="73573-138">-Sku</span></span>
<span data-ttu-id="73573-139">Itt adhatja meg az Azure API-kezelés központi központi telepítéséhez tartozó terület rétegét.</span><span class="sxs-lookup"><span data-stu-id="73573-139">Specifies the tier of the master Azure API Management deployment region.</span></span>
<span data-ttu-id="73573-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="73573-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="73573-141">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="73573-141">Developer</span></span>
- <span data-ttu-id="73573-142">Standard</span><span class="sxs-lookup"><span data-stu-id="73573-142">Standard</span></span>
- <span data-ttu-id="73573-143">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="73573-143">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73573-144">-VirtualNetwork</span></span>
<span data-ttu-id="73573-145">A fő Azure API-kezelési terület virtuális hálózati konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="73573-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="73573-146">-VpnType</span></span>
<span data-ttu-id="73573-147">Az API-kezelés központi telepítését megadó virtuális hálózati típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="73573-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="73573-148">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="73573-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="73573-149">Nincs.</span><span class="sxs-lookup"><span data-stu-id="73573-149">None.</span></span>
<span data-ttu-id="73573-150">Az API-kezelés bevezetése nem része bármely virtuális hálózatnak.</span><span class="sxs-lookup"><span data-stu-id="73573-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="73573-151">Ez az alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="73573-151">This is the default value.</span></span> 
- <span data-ttu-id="73573-152">Külső.</span><span class="sxs-lookup"><span data-stu-id="73573-152">External.</span></span>
<span data-ttu-id="73573-153">Az API-kezelés bevezetésének külső virtuális címe van.</span><span class="sxs-lookup"><span data-stu-id="73573-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="73573-154">Belső.</span><span class="sxs-lookup"><span data-stu-id="73573-154">Internal.</span></span>
<span data-ttu-id="73573-155">Az API-kezelés központi központi elérési környezete intranetes virtuális címet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="73573-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73573-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73573-156">CommonParameters</span></span>
<span data-ttu-id="73573-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73573-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73573-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73573-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73573-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73573-159">INPUTS</span></span>

### <span data-ttu-id="73573-160">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="73573-160">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="73573-161">Paraméterek: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="73573-161">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="73573-162">System. String</span><span class="sxs-lookup"><span data-stu-id="73573-162">System.String</span></span>

### <span data-ttu-id="73573-163">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="73573-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="73573-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="73573-164">System.Int32</span></span>

### <span data-ttu-id="73573-165">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73573-165">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="73573-166">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVpnType</span><span class="sxs-lookup"><span data-stu-id="73573-166">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType</span></span>

### <span data-ttu-id="73573-167">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion, Microsoft. Azure. commands. ApiManagement, Version = 6.1.2.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="73573-167">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="73573-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73573-168">OUTPUTS</span></span>

### <span data-ttu-id="73573-169">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="73573-169">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="73573-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73573-170">NOTES</span></span>

## <span data-ttu-id="73573-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73573-171">RELATED LINKS</span></span>

[<span data-ttu-id="73573-172">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="73573-172">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


