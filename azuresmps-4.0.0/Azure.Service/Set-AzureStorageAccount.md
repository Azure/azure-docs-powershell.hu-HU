---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015850"
---
# <span data-ttu-id="b84ac-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b84ac-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="b84ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b84ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b84ac-103">Egy Azure-előfizetésben frissíti a tárolási fiók tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b84ac-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="b84ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b84ac-104">SYNTAX</span></span>

### <span data-ttu-id="b84ac-105">AccountType (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b84ac-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b84ac-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="b84ac-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b84ac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b84ac-107">DESCRIPTION</span></span>
<span data-ttu-id="b84ac-108">A **set-AzureStorageAccount** parancsmag frissíti az Azure Storage-fiók tulajdonságait az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b84ac-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="b84ac-109">A megadható tulajdonságok: **címke** , **Leírás** , **típus** és **GeoReplicationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="b84ac-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="b84ac-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b84ac-110">EXAMPLES</span></span>

### <span data-ttu-id="b84ac-111">Példa 1: a tárolási fiók címkéjének frissítése</span><span class="sxs-lookup"><span data-stu-id="b84ac-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="b84ac-112">Ez a parancs frissíti a ContosoStorage01 nevű tárterület-fiók **címke** és **Leírás** tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="b84ac-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="b84ac-113">2. példa: a földrajzi replikálás engedélyezése tárolási fiók esetén</span><span class="sxs-lookup"><span data-stu-id="b84ac-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="b84ac-114">Ez a parancs beállítja a **GeoReplicationEnabled** tulajdonságot a ContosoStorage01 nevű tárterület-fiók $false.</span><span class="sxs-lookup"><span data-stu-id="b84ac-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="b84ac-115">3. példa: a Geo-replikáció letiltása tárterület-fiók esetén</span><span class="sxs-lookup"><span data-stu-id="b84ac-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="b84ac-116">Ez a parancs beállítja a **GeoReplicationEnabled** tulajdonságot a ContosoStorage01 nevű tárterület-fiók $True.</span><span class="sxs-lookup"><span data-stu-id="b84ac-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="b84ac-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b84ac-117">PARAMETERS</span></span>

### <span data-ttu-id="b84ac-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b84ac-118">-Description</span></span>
<span data-ttu-id="b84ac-119">A tárterület-fiók leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b84ac-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="b84ac-120">Lehet, hogy a Leírás legfeljebb 1024 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="b84ac-120">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="b84ac-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="b84ac-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="b84ac-122">Meghatározza, hogy a tárolási fiók a Geo-replikációs beállítással van-e létrehozva.</span><span class="sxs-lookup"><span data-stu-id="b84ac-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84ac-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b84ac-123">-InformationAction</span></span>
<span data-ttu-id="b84ac-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b84ac-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b84ac-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b84ac-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b84ac-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b84ac-126">Continue</span></span>
- <span data-ttu-id="b84ac-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b84ac-127">Ignore</span></span>
- <span data-ttu-id="b84ac-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b84ac-128">Inquire</span></span>
- <span data-ttu-id="b84ac-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b84ac-129">SilentlyContinue</span></span>
- <span data-ttu-id="b84ac-130">állj</span><span class="sxs-lookup"><span data-stu-id="b84ac-130">Stop</span></span>
- <span data-ttu-id="b84ac-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b84ac-131">Suspend</span></span>

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

### <span data-ttu-id="b84ac-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b84ac-132">-InformationVariable</span></span>
<span data-ttu-id="b84ac-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b84ac-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b84ac-134">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="b84ac-134">-Label</span></span>
<span data-ttu-id="b84ac-135">A tárolási fiók címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b84ac-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="b84ac-136">Előfordulhat, hogy a címke legfeljebb 100 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="b84ac-136">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="b84ac-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="b84ac-137">-Profile</span></span>
<span data-ttu-id="b84ac-138">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b84ac-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b84ac-139">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b84ac-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b84ac-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b84ac-140">-StorageAccountName</span></span>
<span data-ttu-id="b84ac-141">Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="b84ac-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84ac-142">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="b84ac-142">-Type</span></span>
<span data-ttu-id="b84ac-143">A tárolási fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b84ac-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="b84ac-144">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b84ac-144">Valid values are:</span></span> 

- <span data-ttu-id="b84ac-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="b84ac-145">Standard_LRS</span></span>
- <span data-ttu-id="b84ac-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="b84ac-146">Standard_ZRS</span></span>
- <span data-ttu-id="b84ac-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="b84ac-147">Standard_GRS</span></span>
- <span data-ttu-id="b84ac-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="b84ac-148">Standard_RAGRS</span></span>
- <span data-ttu-id="b84ac-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="b84ac-149">Premium_LRS</span></span>

<span data-ttu-id="b84ac-150">Ha ez a paraméter nincs megadva, az alapértelmezett érték Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="b84ac-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="b84ac-151">A *GeoReplicationEnabled* paraméter megadásának hatása megegyezik a *típus* paraméterben Standard_GRS megadásával.</span><span class="sxs-lookup"><span data-stu-id="b84ac-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="b84ac-152">Standard_ZRS vagy Premium_LRS fiókokat nem lehet más típusú fiókokra módosítani, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="b84ac-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84ac-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84ac-153">CommonParameters</span></span>
<span data-ttu-id="b84ac-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b84ac-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84ac-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b84ac-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84ac-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b84ac-156">INPUTS</span></span>

## <span data-ttu-id="b84ac-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b84ac-157">OUTPUTS</span></span>

## <span data-ttu-id="b84ac-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b84ac-158">NOTES</span></span>

## <span data-ttu-id="b84ac-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b84ac-159">RELATED LINKS</span></span>

[<span data-ttu-id="b84ac-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b84ac-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="b84ac-161">Új – AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b84ac-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="b84ac-162">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b84ac-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


