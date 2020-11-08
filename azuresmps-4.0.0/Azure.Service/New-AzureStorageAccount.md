---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016204"
---
# <span data-ttu-id="ce286-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce286-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="ce286-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce286-102">SYNOPSIS</span></span>
<span data-ttu-id="ce286-103">Új tárolási fiókot hoz létre Azure-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="ce286-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="ce286-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce286-104">SYNTAX</span></span>

### <span data-ttu-id="ce286-105">ParameterSetAffinityGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce286-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ce286-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="ce286-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ce286-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce286-107">DESCRIPTION</span></span>
<span data-ttu-id="ce286-108">A **New-AzureStorageAccount** parancsmag létrehoz egy fiókot, amely hozzáférést biztosít az Azure Storage Services szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ce286-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="ce286-109">A tárterület-fiók globálisan egyedi erőforrás a tárolási rendszeren belül.</span><span class="sxs-lookup"><span data-stu-id="ce286-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="ce286-110">A fiók a blob-, a várólista-és a táblázat-szolgáltatások fölérendelt névtere.</span><span class="sxs-lookup"><span data-stu-id="ce286-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="ce286-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ce286-111">EXAMPLES</span></span>

### <span data-ttu-id="ce286-112">Példa 1: a megadott affinitási csoport tárolási fiókjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="ce286-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="ce286-113">Ez a parancs létrehoz egy tárolási fiókot a megadott affinitási csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="ce286-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="ce286-114">2. példa: tárterület-fiók létrehozása megadott helyen</span><span class="sxs-lookup"><span data-stu-id="ce286-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="ce286-115">A parancs létrehoz egy tárterület-fiókot a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="ce286-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="ce286-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce286-116">PARAMETERS</span></span>

### <span data-ttu-id="ce286-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="ce286-117">-AffinityGroup</span></span>
<span data-ttu-id="ce286-118">Egy meglévő affinitási csoport nevét adja meg az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="ce286-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="ce286-119">Megadhatja a *helyet* vagy a *AffinityGroup* paramétert is, de mindkettőt nem.</span><span class="sxs-lookup"><span data-stu-id="ce286-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ce286-120">-Description</span></span>
<span data-ttu-id="ce286-121">A tárterület-fiók leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce286-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="ce286-122">A Leírás legfeljebb 1024 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="ce286-122">The description may be up to 1024 characters in length.</span></span>

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

### <span data-ttu-id="ce286-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ce286-123">-InformationAction</span></span>
<span data-ttu-id="ce286-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ce286-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ce286-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ce286-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce286-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ce286-126">Continue</span></span>
- <span data-ttu-id="ce286-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ce286-127">Ignore</span></span>
- <span data-ttu-id="ce286-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ce286-128">Inquire</span></span>
- <span data-ttu-id="ce286-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ce286-129">SilentlyContinue</span></span>
- <span data-ttu-id="ce286-130">állj</span><span class="sxs-lookup"><span data-stu-id="ce286-130">Stop</span></span>
- <span data-ttu-id="ce286-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ce286-131">Suspend</span></span>

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

### <span data-ttu-id="ce286-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ce286-132">-InformationVariable</span></span>
<span data-ttu-id="ce286-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ce286-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ce286-134">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="ce286-134">-Label</span></span>
<span data-ttu-id="ce286-135">A tárolási fiók címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce286-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="ce286-136">Előfordulhat, hogy a címke hossza legfeljebb 100 karakter lehet.</span><span class="sxs-lookup"><span data-stu-id="ce286-136">The label may be up to 100 characters in length.</span></span>

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

### <span data-ttu-id="ce286-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="ce286-137">-Location</span></span>
<span data-ttu-id="ce286-138">Az Azure Data Center helyét adja meg, ahol a tárolási fiók létrejön.</span><span class="sxs-lookup"><span data-stu-id="ce286-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="ce286-139">A *helyet* vagy a *AffinityGroup* paramétert is megadhatja, de mindkettőt nem.</span><span class="sxs-lookup"><span data-stu-id="ce286-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="ce286-140">-Profile</span></span>
<span data-ttu-id="ce286-141">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ce286-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce286-142">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ce286-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce286-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ce286-143">-StorageAccountName</span></span>
<span data-ttu-id="ce286-144">A tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce286-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="ce286-145">A tárolási fiók nevének egyedinek kell lennie az Azure-ban, és a hosszúság 3 és 24 karakter közé kell lennie, és csak kis betűket és számokat kell használnia.</span><span class="sxs-lookup"><span data-stu-id="ce286-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-146">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ce286-146">-Type</span></span>
<span data-ttu-id="ce286-147">A tárolási fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce286-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="ce286-148">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ce286-148">Valid values are:</span></span>

- <span data-ttu-id="ce286-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="ce286-149">Standard_LRS</span></span>
- <span data-ttu-id="ce286-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="ce286-150">Standard_ZRS</span></span>
- <span data-ttu-id="ce286-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="ce286-151">Standard_GRS</span></span>
- <span data-ttu-id="ce286-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="ce286-152">Standard_RAGRS</span></span>
- <span data-ttu-id="ce286-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="ce286-153">Premium_LRS</span></span>

<span data-ttu-id="ce286-154">Ha ez a paraméter nincs megadva, az alapértelmezett érték Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="ce286-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="ce286-155">Standard_ZRS vagy Premium_LRS fiókokat nem lehet más típusú fiókokra módosítani, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="ce286-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce286-156">CommonParameters</span></span>
<span data-ttu-id="ce286-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce286-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce286-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce286-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce286-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce286-159">INPUTS</span></span>

## <span data-ttu-id="ce286-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce286-160">OUTPUTS</span></span>

## <span data-ttu-id="ce286-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce286-161">NOTES</span></span>

## <span data-ttu-id="ce286-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce286-162">RELATED LINKS</span></span>

[<span data-ttu-id="ce286-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce286-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="ce286-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce286-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


