---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015844"
---
# <span data-ttu-id="89ee6-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89ee6-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="89ee6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="89ee6-103">Az alkalmazás-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="89ee6-103">Updates an application gateway.</span></span>

## <span data-ttu-id="89ee6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89ee6-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89ee6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89ee6-105">DESCRIPTION</span></span>
<span data-ttu-id="89ee6-106">Az **Update-AzureApplicationGateway** parancsmag egy meglévő alkalmazás-átjárót frissít.</span><span class="sxs-lookup"><span data-stu-id="89ee6-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="89ee6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89ee6-107">EXAMPLES</span></span>

### <span data-ttu-id="89ee6-108">1. példa: az alkalmazás átjárójának módosítása a neve alapján</span><span class="sxs-lookup"><span data-stu-id="89ee6-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="89ee6-109">Az első parancs leállítja a ApplicationGateway06 nevű alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="89ee6-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="89ee6-110">A virtuális hálózat vagy alhálózatok módosítása előtt le kell állítani egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="89ee6-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="89ee6-111">A második parancs módosítja a ApplicationGateway06 nevű alkalmazás-átjáró virtuális alhálózatát és alhálózatait.</span><span class="sxs-lookup"><span data-stu-id="89ee6-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="89ee6-112">2. példa: az alkalmazás-átjáró további tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="89ee6-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="89ee6-113">Ez a parancs módosítja a ApplicationGateway06 nevű alkalmazás-átjáró példányának számát, az átjáró méretét és leírását.</span><span class="sxs-lookup"><span data-stu-id="89ee6-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="89ee6-114">Ez a parancs nem módosítja az Application Gateway virtuális hálózatát vagy alhálózatait.</span><span class="sxs-lookup"><span data-stu-id="89ee6-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="89ee6-115">Ezért a parancs futtatása előtt nem kell leállítania az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="89ee6-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="89ee6-116">3. példa: az alkalmazás-átjárók módosítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="89ee6-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="89ee6-117">Az első parancs a **Get-AzureApplicationGateway** parancsmag használatával kapja meg a ApplicationGateway06 nevű alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="89ee6-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="89ee6-118">A parancs a $ApplicationGateway változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89ee6-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="89ee6-119">A második parancs a **GatewaySize** tulajdonságot a Medium értékre osztja.</span><span class="sxs-lookup"><span data-stu-id="89ee6-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="89ee6-120">A végleges parancs átadja a frissített $ApplicationGateway az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="89ee6-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="89ee6-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89ee6-121">PARAMETERS</span></span>

### <span data-ttu-id="89ee6-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="89ee6-122">-Description</span></span>
<span data-ttu-id="89ee6-123">Azt a leírást adja meg, amelyet a parancsmag az alkalmazás-átjáróhoz rendel.</span><span class="sxs-lookup"><span data-stu-id="89ee6-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="89ee6-124">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="89ee6-124">-GatewaySize</span></span>
<span data-ttu-id="89ee6-125">Azt adja meg, hogy a parancsmag milyen méretet rendel az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="89ee6-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="89ee6-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="89ee6-126">Valid values are:</span></span>

- <span data-ttu-id="89ee6-127">Kisvállalati</span><span class="sxs-lookup"><span data-stu-id="89ee6-127">Small</span></span>
- <span data-ttu-id="89ee6-128">Közepes</span><span class="sxs-lookup"><span data-stu-id="89ee6-128">Medium</span></span>
- <span data-ttu-id="89ee6-129">Nagy</span><span class="sxs-lookup"><span data-stu-id="89ee6-129">Large</span></span>

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

### <span data-ttu-id="89ee6-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="89ee6-130">-InstanceCount</span></span>
<span data-ttu-id="89ee6-131">Azt adja meg, hogy a parancsmag hány példányt rendel az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="89ee6-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="89ee6-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89ee6-132">-Name</span></span>
<span data-ttu-id="89ee6-133">Annak az alkalmazási átjárónak a nevét adja meg, amely a parancsmag által frissült.</span><span class="sxs-lookup"><span data-stu-id="89ee6-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

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

### <span data-ttu-id="89ee6-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="89ee6-134">-Profile</span></span>
<span data-ttu-id="89ee6-135">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="89ee6-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89ee6-136">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="89ee6-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89ee6-137">-Alhálózatok</span><span class="sxs-lookup"><span data-stu-id="89ee6-137">-Subnets</span></span>
<span data-ttu-id="89ee6-138">Itt adhatja meg azt az alhálózatokat, amelyben ez a parancsmag telepíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="89ee6-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="89ee6-139">Nem frissíthetők az alhálózatok, miközben az alkalmazás-átjáró fut.</span><span class="sxs-lookup"><span data-stu-id="89ee6-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="89ee6-140">Az alkalmazás-átjáró leállításához használja az Stop-AzureApplicationGateway parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89ee6-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ee6-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="89ee6-141">-VnetName</span></span>
<span data-ttu-id="89ee6-142">Annak a virtuális hálózatnak a meghatározása, amelyben ez a parancsmag telepíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="89ee6-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="89ee6-143">A virtuális hálózatokat nem frissítheti, miközben az alkalmazás-átjáró fut.</span><span class="sxs-lookup"><span data-stu-id="89ee6-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="89ee6-144">Az alkalmazás-átjáró leállításához használja a **stop-AzureApplicationGateway**.</span><span class="sxs-lookup"><span data-stu-id="89ee6-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

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

### <span data-ttu-id="89ee6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ee6-145">CommonParameters</span></span>
<span data-ttu-id="89ee6-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89ee6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ee6-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ee6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ee6-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89ee6-148">INPUTS</span></span>

### <span data-ttu-id="89ee6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="89ee6-149">System.String</span></span>

## <span data-ttu-id="89ee6-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89ee6-150">OUTPUTS</span></span>

### <span data-ttu-id="89ee6-151">Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="89ee6-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="89ee6-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89ee6-152">NOTES</span></span>

## <span data-ttu-id="89ee6-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89ee6-153">RELATED LINKS</span></span>

[<span data-ttu-id="89ee6-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89ee6-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="89ee6-155">Új – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89ee6-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="89ee6-156">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89ee6-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="89ee6-157">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89ee6-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="89ee6-158">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89ee6-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)
