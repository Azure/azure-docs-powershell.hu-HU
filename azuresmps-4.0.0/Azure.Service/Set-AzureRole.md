---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015824"
---
# <span data-ttu-id="9efd8-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="9efd8-101">Set-AzureRole</span></span>

## <span data-ttu-id="9efd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9efd8-102">SYNOPSIS</span></span>
<span data-ttu-id="9efd8-103">Megadja, hogy az Azure-szerepkörök példányai hány példányban fussanak.</span><span class="sxs-lookup"><span data-stu-id="9efd8-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="9efd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9efd8-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9efd8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9efd8-105">DESCRIPTION</span></span>
<span data-ttu-id="9efd8-106">A **set-AzureRole** parancsmag azt adja meg, hogy egy adott szerepkör példányai hány példányban futnak az Azure-példányban.</span><span class="sxs-lookup"><span data-stu-id="9efd8-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="9efd8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9efd8-107">EXAMPLES</span></span>

### <span data-ttu-id="9efd8-108">1: egy szerepkör példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9efd8-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="9efd8-109">Ez a parancs a MySvc01 szolgáltatásban futó MyTestRole03 szerepkört három példányra állítja be.</span><span class="sxs-lookup"><span data-stu-id="9efd8-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="9efd8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9efd8-110">PARAMETERS</span></span>

### <span data-ttu-id="9efd8-111">-Count</span><span class="sxs-lookup"><span data-stu-id="9efd8-111">-Count</span></span>
<span data-ttu-id="9efd8-112">A futtatandó szerepkör-példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9efd8-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9efd8-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9efd8-113">-InformationAction</span></span>
<span data-ttu-id="9efd8-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="9efd8-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9efd8-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9efd8-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9efd8-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="9efd8-116">Continue</span></span>
- <span data-ttu-id="9efd8-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="9efd8-117">Ignore</span></span>
- <span data-ttu-id="9efd8-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="9efd8-118">Inquire</span></span>
- <span data-ttu-id="9efd8-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9efd8-119">SilentlyContinue</span></span>
- <span data-ttu-id="9efd8-120">állj</span><span class="sxs-lookup"><span data-stu-id="9efd8-120">Stop</span></span>
- <span data-ttu-id="9efd8-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="9efd8-121">Suspend</span></span>

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

### <span data-ttu-id="9efd8-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9efd8-122">-InformationVariable</span></span>
<span data-ttu-id="9efd8-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="9efd8-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9efd8-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="9efd8-124">-Profile</span></span>
<span data-ttu-id="9efd8-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9efd8-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9efd8-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9efd8-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9efd8-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="9efd8-127">-RoleName</span></span>
<span data-ttu-id="9efd8-128">Annak a szerepkörnek a neve, amelyhez a példányok számát be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="9efd8-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efd8-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="9efd8-129">-ServiceName</span></span>
<span data-ttu-id="9efd8-130">Az Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9efd8-130">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="9efd8-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="9efd8-131">-Slot</span></span>
<span data-ttu-id="9efd8-132">A módosításhoz használt központi telepítő környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9efd8-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="9efd8-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9efd8-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9efd8-134">Production</span><span class="sxs-lookup"><span data-stu-id="9efd8-134">Production</span></span>
- <span data-ttu-id="9efd8-135">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="9efd8-135">Staging</span></span>

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

### <span data-ttu-id="9efd8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9efd8-136">CommonParameters</span></span>
<span data-ttu-id="9efd8-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9efd8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9efd8-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9efd8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9efd8-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9efd8-139">INPUTS</span></span>

## <span data-ttu-id="9efd8-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9efd8-140">OUTPUTS</span></span>

## <span data-ttu-id="9efd8-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9efd8-141">NOTES</span></span>

## <span data-ttu-id="9efd8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9efd8-142">RELATED LINKS</span></span>

[<span data-ttu-id="9efd8-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="9efd8-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


