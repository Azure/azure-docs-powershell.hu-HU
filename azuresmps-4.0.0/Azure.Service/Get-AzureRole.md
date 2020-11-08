---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016314"
---
# <span data-ttu-id="12c24-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="12c24-101">Get-AzureRole</span></span>

## <span data-ttu-id="12c24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12c24-102">SYNOPSIS</span></span>
<span data-ttu-id="12c24-103">A Microsoft Azure-szolgáltatás szerepköreinek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="12c24-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="12c24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12c24-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="12c24-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12c24-105">DESCRIPTION</span></span>
<span data-ttu-id="12c24-106">A **Get-AzureRole** parancsmag egy lista-objektumot ad eredményül, amely a Microsoft Azure-szolgáltatás szerepköreinek részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="12c24-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="12c24-107">Ha a *RoleName* paramétert adja meg, a **Get-AzureRole** csak az adott szerepkör adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="12c24-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="12c24-108">Ha a *InstanceDetails* paramétert adja meg, a függvény további, példány-specifikus részleteket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="12c24-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="12c24-109">Példák</span><span class="sxs-lookup"><span data-stu-id="12c24-109">EXAMPLES</span></span>

### <span data-ttu-id="12c24-110">Példa 1: a szolgáltatások szerepkörének beszerzése</span><span class="sxs-lookup"><span data-stu-id="12c24-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="12c24-111">Ez a parancs egy olyan objektumot ad eredményül, amely részletesen ismerteti az MySvc01 szolgáltatásban futó összes termelési szerepkört.</span><span class="sxs-lookup"><span data-stu-id="12c24-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="12c24-112">2. példa: adatok beszerzése a szolgáltatáson futó szerepkörökről</span><span class="sxs-lookup"><span data-stu-id="12c24-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="12c24-113">Ez a parancs egy olyan objektumot ad eredményül, amely a MyTestVM3 szerepkör részleteit jeleníti meg a MySvc01 szolgáltatás átmeneti környezetében.</span><span class="sxs-lookup"><span data-stu-id="12c24-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="12c24-114">3. példa: a szolgáltatásban futó szerepkör példányaira vonatkozó információk beszerzése</span><span class="sxs-lookup"><span data-stu-id="12c24-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="12c24-115">Ez a parancs egy olyan objektumot ad eredményül, amely részletesen ismerteti az MyTestVM02 szerepkör példányait a MySvc01 szolgáltatás üzemi környezetében.</span><span class="sxs-lookup"><span data-stu-id="12c24-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="12c24-116">Példa 4: a szolgáltatáshoz társított szerepkör-példányok táblázatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="12c24-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="12c24-117">Ez a parancs visszaadja az MySvc01 szolgáltatás üzemi környezetében futó minden szerepkör-példány példányának nevét, méretét és állapotát.</span><span class="sxs-lookup"><span data-stu-id="12c24-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="12c24-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12c24-118">PARAMETERS</span></span>

### <span data-ttu-id="12c24-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="12c24-119">-InformationAction</span></span>
<span data-ttu-id="12c24-120">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="12c24-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="12c24-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="12c24-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12c24-122">Folytassa</span><span class="sxs-lookup"><span data-stu-id="12c24-122">Continue</span></span>
- <span data-ttu-id="12c24-123">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="12c24-123">Ignore</span></span>
- <span data-ttu-id="12c24-124">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="12c24-124">Inquire</span></span>
- <span data-ttu-id="12c24-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="12c24-125">SilentlyContinue</span></span>
- <span data-ttu-id="12c24-126">állj</span><span class="sxs-lookup"><span data-stu-id="12c24-126">Stop</span></span>
- <span data-ttu-id="12c24-127">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="12c24-127">Suspend</span></span>

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

### <span data-ttu-id="12c24-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="12c24-128">-InformationVariable</span></span>
<span data-ttu-id="12c24-129">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="12c24-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="12c24-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="12c24-130">-InstanceDetails</span></span>
<span data-ttu-id="12c24-131">Azt adja meg, hogy a parancsmag az egyes szerepkörök példányairól adja meg az adatokat.</span><span class="sxs-lookup"><span data-stu-id="12c24-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12c24-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="12c24-132">-Profile</span></span>
<span data-ttu-id="12c24-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="12c24-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12c24-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="12c24-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12c24-135">-RoleName</span><span class="sxs-lookup"><span data-stu-id="12c24-135">-RoleName</span></span>
<span data-ttu-id="12c24-136">A beolvasott szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12c24-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12c24-137">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="12c24-137">-ServiceName</span></span>
<span data-ttu-id="12c24-138">Az Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12c24-138">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="12c24-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="12c24-139">-Slot</span></span>
<span data-ttu-id="12c24-140">Az Azure-telepítő környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12c24-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="12c24-141">A paraméter elfogadható értékei a következők: termelés vagy megállóhely.</span><span class="sxs-lookup"><span data-stu-id="12c24-141">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12c24-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c24-142">CommonParameters</span></span>
<span data-ttu-id="12c24-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12c24-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c24-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c24-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c24-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12c24-145">INPUTS</span></span>

## <span data-ttu-id="12c24-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12c24-146">OUTPUTS</span></span>

## <span data-ttu-id="12c24-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12c24-147">NOTES</span></span>

## <span data-ttu-id="12c24-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12c24-148">RELATED LINKS</span></span>

[<span data-ttu-id="12c24-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="12c24-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


