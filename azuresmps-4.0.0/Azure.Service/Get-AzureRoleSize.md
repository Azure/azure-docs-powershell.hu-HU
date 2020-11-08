---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015615"
---
# <span data-ttu-id="805e5-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="805e5-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="805e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="805e5-102">SYNOPSIS</span></span>
<span data-ttu-id="805e5-103">A jelenlegi előfizetéshez tartozó szerepkör-méret adatainak lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="805e5-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="805e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="805e5-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="805e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="805e5-105">DESCRIPTION</span></span>
<span data-ttu-id="805e5-106">A **Get-AzureRoleSize** parancsmag a jelenlegi előfizetés szerepkör-méretére vonatkozó információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="805e5-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="805e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="805e5-107">EXAMPLES</span></span>

### <span data-ttu-id="805e5-108">Példa 1: a szerepkör méretére vonatkozó információk beszerzése</span><span class="sxs-lookup"><span data-stu-id="805e5-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="805e5-109">Ez a parancs a jelenlegi előfizetés szerepkör-méretre vonatkozó adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="805e5-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="805e5-110">2. példa: a szerepkörök méretének beolvasása és a szerepkör méretének megadása</span><span class="sxs-lookup"><span data-stu-id="805e5-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="805e5-111">Ez a parancs a megadott szerepkör-méretre vonatkozó információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="805e5-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="805e5-112">3. példa: a szerepkörök méretére vonatkozó információk beszerzése az összes virtuális gépre az Azure Services szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="805e5-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="805e5-113">Ez a parancs az Azure összes szolgáltatásában a virtuális gépekhez tartozó szerepkör-méretre vonatkozó információkat kapja.</span><span class="sxs-lookup"><span data-stu-id="805e5-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="805e5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="805e5-114">PARAMETERS</span></span>

### <span data-ttu-id="805e5-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="805e5-115">-InformationAction</span></span>
<span data-ttu-id="805e5-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="805e5-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="805e5-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="805e5-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="805e5-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="805e5-118">Continue</span></span>
- <span data-ttu-id="805e5-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="805e5-119">Ignore</span></span>
- <span data-ttu-id="805e5-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="805e5-120">Inquire</span></span>
- <span data-ttu-id="805e5-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="805e5-121">SilentlyContinue</span></span>
- <span data-ttu-id="805e5-122">állj</span><span class="sxs-lookup"><span data-stu-id="805e5-122">Stop</span></span>
- <span data-ttu-id="805e5-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="805e5-123">Suspend</span></span>

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

### <span data-ttu-id="805e5-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="805e5-124">-InformationVariable</span></span>
<span data-ttu-id="805e5-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="805e5-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="805e5-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="805e5-126">-InstanceSize</span></span>
<span data-ttu-id="805e5-127">A szerepkör méretének nevét adja meg, például: ExtraSmall, kicsi, nagy, ExtraLarge, a5, A6, A7.</span><span class="sxs-lookup"><span data-stu-id="805e5-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805e5-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="805e5-128">-Profile</span></span>
<span data-ttu-id="805e5-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="805e5-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="805e5-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="805e5-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="805e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805e5-131">CommonParameters</span></span>
<span data-ttu-id="805e5-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="805e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805e5-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="805e5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805e5-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="805e5-134">INPUTS</span></span>

## <span data-ttu-id="805e5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="805e5-135">OUTPUTS</span></span>

## <span data-ttu-id="805e5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="805e5-136">NOTES</span></span>

## <span data-ttu-id="805e5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="805e5-137">RELATED LINKS</span></span>

[<span data-ttu-id="805e5-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="805e5-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="805e5-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="805e5-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="805e5-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="805e5-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


