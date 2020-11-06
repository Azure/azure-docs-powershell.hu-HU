---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 2022a8a830d868f412e505f23e65c4c297bea543
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505171"
---
# <span data-ttu-id="e52e4-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e52e4-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="e52e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e52e4-102">SYNOPSIS</span></span>
<span data-ttu-id="e52e4-103">Konfigurálható virtuálisgép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e52e4-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e52e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e52e4-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [[-IdentityType] <ResourceIdentityType>] [-AssignIdentity] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e52e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e52e4-105">DESCRIPTION</span></span>
<span data-ttu-id="e52e4-106">A **New-AzureRmVMConfig** parancsmag létrehoz egy konfigurálható helyi virtuálisgép-objektumot az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="e52e4-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="e52e4-107">Az egyéb parancsmagok segítségével konfigurálhatók a virtuálisgép-objektumok, például a set-AzureRmVMOperatingSystem, a set-AzureRmVMSourceImage, a Add-AzureRmVMNetworkInterface és a set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="e52e4-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="e52e4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e52e4-108">EXAMPLES</span></span>

### <span data-ttu-id="e52e4-109">Példa 1: virtuális gép objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e52e4-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="e52e4-110">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="e52e4-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="e52e4-111">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e52e4-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e52e4-112">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="e52e4-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e52e4-113">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="e52e4-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="e52e4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e52e4-114">PARAMETERS</span></span>

### <span data-ttu-id="e52e4-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e52e4-115">-AssignIdentity</span></span>
<span data-ttu-id="e52e4-116">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="e52e4-116">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52e4-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="e52e4-117">-AvailabilitySetId</span></span>
<span data-ttu-id="e52e4-118">A rendelkezésre álló készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e52e4-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="e52e4-119">Az elérhetőségi készlet objektum beolvasásához használja az Get-AzureRmAvailabilitySet parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e52e4-119">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="e52e4-120">Az elérhetőségi készlet objektum egy azonosító tulajdonságot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e52e4-120">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e52e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e52e4-121">-DefaultProfile</span></span>
<span data-ttu-id="e52e4-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e52e4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e52e4-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e52e4-123">-IdentityType</span></span>
<span data-ttu-id="e52e4-124">A virtuális gép identitása, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="e52e4-124">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52e4-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e52e4-125">-LicenseType</span></span>
<span data-ttu-id="e52e4-126">A licenc típusa, amely a saját licenc-forgatókönyv készítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="e52e4-126">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52e4-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="e52e4-127">-Tags</span></span>
<span data-ttu-id="e52e4-128">Az erőforráshoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="e52e4-128">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e52e4-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="e52e4-129">-VMName</span></span>
<span data-ttu-id="e52e4-130">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e52e4-130">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e52e4-131">-VMSize</span><span class="sxs-lookup"><span data-stu-id="e52e4-131">-VMSize</span></span>
<span data-ttu-id="e52e4-132">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e52e4-132">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="e52e4-133">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="e52e4-133">-Zone</span></span>
<span data-ttu-id="e52e4-134">A virtuális gép zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e52e4-134">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e52e4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52e4-135">CommonParameters</span></span>
<span data-ttu-id="e52e4-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e52e4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52e4-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e52e4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52e4-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e52e4-138">INPUTS</span></span>

## <span data-ttu-id="e52e4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e52e4-139">OUTPUTS</span></span>

## <span data-ttu-id="e52e4-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e52e4-140">NOTES</span></span>

## <span data-ttu-id="e52e4-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e52e4-141">RELATED LINKS</span></span>

[<span data-ttu-id="e52e4-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e52e4-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="e52e4-143">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e52e4-143">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="e52e4-144">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="e52e4-144">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="e52e4-145">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e52e4-145">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


