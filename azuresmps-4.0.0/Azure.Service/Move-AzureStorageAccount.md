---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016239"
---
# <span data-ttu-id="40d42-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40d42-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="40d42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40d42-102">SYNOPSIS</span></span>
<span data-ttu-id="40d42-103">Áttelepíti a tárolási fiókot az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="40d42-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="40d42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40d42-104">SYNTAX</span></span>

### <span data-ttu-id="40d42-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d42-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="40d42-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d42-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="40d42-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d42-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="40d42-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d42-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="40d42-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="40d42-109">DESCRIPTION</span></span>
<span data-ttu-id="40d42-110">A **Move-AzureStorageAccount** parancsmag az Azure Resource Manager-kötegben lévő erőforrás-csoportba telepíti a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="40d42-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="40d42-111">Példák</span><span class="sxs-lookup"><span data-stu-id="40d42-111">EXAMPLES</span></span>

### <span data-ttu-id="40d42-112">1. példa: a tárolási fiók áttelepítésének előkészítése</span><span class="sxs-lookup"><span data-stu-id="40d42-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="40d42-113">Ez a parancs a ContosoStorageName nevű tárolási fiókot készíti elő az Azure Resource Manager-kötegbe való áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="40d42-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="40d42-114">2. példa: a tárolási fiók áttelepítésének megkezdése</span><span class="sxs-lookup"><span data-stu-id="40d42-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="40d42-115">Ez a parancs elindítja a ContosoStorageName nevű tárolási fiók áttelepítését az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="40d42-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="40d42-116">3. példa: a tárolási fiók áttelepítésének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="40d42-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="40d42-117">Ez a parancs ellenőrzi a ContosoStorageName nevű tárolási fiók áttelepítését az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="40d42-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="40d42-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40d42-118">PARAMETERS</span></span>

### <span data-ttu-id="40d42-119">-Megszakítás</span><span class="sxs-lookup"><span data-stu-id="40d42-119">-Abort</span></span>
<span data-ttu-id="40d42-120">Jelzi, hogy ez a parancsmag lemondja a tárolási fiók áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="40d42-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d42-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="40d42-121">-Commit</span></span>
<span data-ttu-id="40d42-122">Azt jelzi, hogy ez a parancsmag elindítja a tárolási fiók áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="40d42-122">Indicates that this cmdlet starts the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d42-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="40d42-123">-InformationAction</span></span>
<span data-ttu-id="40d42-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="40d42-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="40d42-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="40d42-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="40d42-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="40d42-126">Continue</span></span>
- <span data-ttu-id="40d42-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="40d42-127">Ignore</span></span>
- <span data-ttu-id="40d42-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="40d42-128">Inquire</span></span>
- <span data-ttu-id="40d42-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="40d42-129">SilentlyContinue</span></span>
- <span data-ttu-id="40d42-130">állj</span><span class="sxs-lookup"><span data-stu-id="40d42-130">Stop</span></span>
- <span data-ttu-id="40d42-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="40d42-131">Suspend</span></span>

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

### <span data-ttu-id="40d42-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="40d42-132">-InformationVariable</span></span>
<span data-ttu-id="40d42-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="40d42-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="40d42-134">– Előkészületek</span><span class="sxs-lookup"><span data-stu-id="40d42-134">-Prepare</span></span>
<span data-ttu-id="40d42-135">Jelzi, hogy ez a parancsmag előkészíti a tárolási fiókot az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="40d42-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d42-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="40d42-136">-Profile</span></span>
<span data-ttu-id="40d42-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="40d42-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40d42-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="40d42-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40d42-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="40d42-139">-StorageAccountName</span></span>
<span data-ttu-id="40d42-140">Annak a tároló fióknak a nevét adja meg, amelyre a parancsmag át van telepítve.</span><span class="sxs-lookup"><span data-stu-id="40d42-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="40d42-141">– Érvényesítés</span><span class="sxs-lookup"><span data-stu-id="40d42-141">-Validate</span></span>
<span data-ttu-id="40d42-142">Meghatározza, hogy ez a parancsmag ellenőrzi-e az áttelepítés tárolási fiókját.</span><span class="sxs-lookup"><span data-stu-id="40d42-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d42-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d42-143">CommonParameters</span></span>
<span data-ttu-id="40d42-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40d42-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d42-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d42-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d42-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40d42-146">INPUTS</span></span>

## <span data-ttu-id="40d42-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40d42-147">OUTPUTS</span></span>

## <span data-ttu-id="40d42-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40d42-148">NOTES</span></span>

## <span data-ttu-id="40d42-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40d42-149">RELATED LINKS</span></span>

[<span data-ttu-id="40d42-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="40d42-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="40d42-151">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="40d42-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="40d42-152">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="40d42-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="40d42-153">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="40d42-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="40d42-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40d42-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


