---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016165"
---
# <span data-ttu-id="67037-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="67037-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="67037-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67037-102">SYNOPSIS</span></span>
<span data-ttu-id="67037-103">Törli a Felhőbeli szolgáltatások üzembe helyezését.</span><span class="sxs-lookup"><span data-stu-id="67037-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="67037-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67037-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="67037-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67037-105">DESCRIPTION</span></span>
<span data-ttu-id="67037-106">A **Remove-AzureDeployment** parancsmag törli az Azure Cloud-szolgáltatás telepítését.</span><span class="sxs-lookup"><span data-stu-id="67037-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="67037-107">Ha törölni szeretne egy központi telepítőt, először függessze fel.</span><span class="sxs-lookup"><span data-stu-id="67037-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="67037-108">Példák</span><span class="sxs-lookup"><span data-stu-id="67037-108">EXAMPLES</span></span>

### <span data-ttu-id="67037-109">1. példa: a központi telepítő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="67037-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="67037-110">Ez a parancs eltávolítja a ContosoService nevű Azure szolgáltatás telepítését.</span><span class="sxs-lookup"><span data-stu-id="67037-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="67037-111">Mivel a parancs nem ad meg tárolóhelyet, eltávolítja a szolgáltatást a termelési környezetből.</span><span class="sxs-lookup"><span data-stu-id="67037-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="67037-112">2. példa: a központi telepítések és a virtuális merevlemezek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="67037-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="67037-113">Ez a parancs eltávolítja a ContosoService nevű szolgáltatás telepítését a termelési környezetből.</span><span class="sxs-lookup"><span data-stu-id="67037-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="67037-114">A parancs a mögöttes virtuális merevlemezeket is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="67037-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="67037-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67037-115">PARAMETERS</span></span>

### <span data-ttu-id="67037-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="67037-116">-DeleteVHD</span></span>
<span data-ttu-id="67037-117">Megadja, hogy a parancsmag eltávolítja a telepítőt és a virtuális merevlemezeket (VHD-ket) a blob-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="67037-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67037-118">-Force</span><span class="sxs-lookup"><span data-stu-id="67037-118">-Force</span></span>
<span data-ttu-id="67037-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="67037-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67037-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="67037-120">-InformationAction</span></span>
<span data-ttu-id="67037-121">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="67037-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="67037-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="67037-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67037-123">Folytassa</span><span class="sxs-lookup"><span data-stu-id="67037-123">Continue</span></span>
- <span data-ttu-id="67037-124">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="67037-124">Ignore</span></span>
- <span data-ttu-id="67037-125">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="67037-125">Inquire</span></span>
- <span data-ttu-id="67037-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="67037-126">SilentlyContinue</span></span>
- <span data-ttu-id="67037-127">állj</span><span class="sxs-lookup"><span data-stu-id="67037-127">Stop</span></span>
- <span data-ttu-id="67037-128">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="67037-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67037-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="67037-129">-InformationVariable</span></span>
<span data-ttu-id="67037-130">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="67037-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67037-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="67037-131">-Profile</span></span>
<span data-ttu-id="67037-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="67037-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67037-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="67037-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67037-134">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="67037-134">-ServiceName</span></span>
<span data-ttu-id="67037-135">Annak a szolgáltatásnak a nevét adja meg, amelyre ez a parancsmag törli a telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="67037-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

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

### <span data-ttu-id="67037-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="67037-136">-Slot</span></span>
<span data-ttu-id="67037-137">Azt a központi telepítő környezetet adja meg, amelyből a parancsmag törli a központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="67037-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="67037-138">Érvényes értékek: staging és termelés.</span><span class="sxs-lookup"><span data-stu-id="67037-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="67037-139">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="67037-139">The default value is Production.</span></span>

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

### <span data-ttu-id="67037-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67037-140">CommonParameters</span></span>
<span data-ttu-id="67037-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67037-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67037-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67037-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67037-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67037-143">INPUTS</span></span>

## <span data-ttu-id="67037-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67037-144">OUTPUTS</span></span>

### <span data-ttu-id="67037-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="67037-145">ManagementOperationContext</span></span>

## <span data-ttu-id="67037-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67037-146">NOTES</span></span>

## <span data-ttu-id="67037-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67037-147">RELATED LINKS</span></span>

[<span data-ttu-id="67037-148">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="67037-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="67037-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="67037-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="67037-150">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="67037-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="67037-151">Új – AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="67037-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="67037-152">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="67037-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


