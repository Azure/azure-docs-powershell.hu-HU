---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015551"
---
# <span data-ttu-id="cfa47-101">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cfa47-101">Get-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="cfa47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfa47-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa47-103">Hitelesítő adatokkal kapja meg a tárolási fiókokat.</span><span class="sxs-lookup"><span data-stu-id="cfa47-103">Gets credentials for storage accounts.</span></span>

## <span data-ttu-id="cfa47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfa47-104">SYNTAX</span></span>

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfa47-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfa47-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa47-106">A **Get-AzureStorSimpleStorageAccountCredential** parancsmag hitelesítő adatokat kap a tárolási fiókokhoz.</span><span class="sxs-lookup"><span data-stu-id="cfa47-106">The **Get-AzureStorSimpleStorageAccountCredential** cmdlet gets credentials for storage accounts.</span></span>
<span data-ttu-id="cfa47-107">Ez a parancsmag a szolgáltatásban vagy egy névvel ellátott **StorageAccountCredential** konfigurált összes **StorageAccountCredential** -objektumot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="cfa47-107">This cmdlet gets all **StorageAccountCredential** objects configured in the service or a named **StorageAccountCredential**.</span></span>

## <span data-ttu-id="cfa47-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cfa47-108">EXAMPLES</span></span>

### <span data-ttu-id="cfa47-109">Példa 1: az erőforrás összes hitelesítő adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="cfa47-109">Example 1: Get all credentials for a resource</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

<span data-ttu-id="cfa47-110">Ez a parancs az aktuális erőforrás tárolási fiókjaihoz elérhető hitelesítő adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cfa47-110">This command gets all available credentials for storage accounts for the current resource.</span></span>

### <span data-ttu-id="cfa47-111">2. példa: a hitelesítő adatok beszerzése egy adott tárolási fiókhoz</span><span class="sxs-lookup"><span data-stu-id="cfa47-111">Example 2: Get the credential for a specific storage account</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

<span data-ttu-id="cfa47-112">Ez a parancs beolvassa a ContosoCloudStorage nevű tárolási fiókhoz tartozó tárolási fiók hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="cfa47-112">This command gets the storage account credential for the storage account named ContosoCloudStorage.</span></span>

## <span data-ttu-id="cfa47-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfa47-113">PARAMETERS</span></span>

### <span data-ttu-id="cfa47-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="cfa47-114">-Profile</span></span>
<span data-ttu-id="cfa47-115">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="cfa47-115">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="cfa47-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cfa47-116">-StorageAccountName</span></span>
<span data-ttu-id="cfa47-117">Annak a tároló fióknak a nevét adja meg, amelyhez hitelesítő adatokat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="cfa47-117">Specifies the name of the storage account for which to get credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa47-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa47-118">CommonParameters</span></span>
<span data-ttu-id="cfa47-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfa47-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa47-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa47-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa47-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfa47-121">INPUTS</span></span>

### <span data-ttu-id="cfa47-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="cfa47-122">None</span></span>

## <span data-ttu-id="cfa47-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfa47-123">OUTPUTS</span></span>

### <span data-ttu-id="cfa47-124">StorageAccountCredential, IList\<StorageAccountCredential\></span><span class="sxs-lookup"><span data-stu-id="cfa47-124">StorageAccountCredential, IList\<StorageAccountCredential\></span></span>
<span data-ttu-id="cfa47-125">Ez a parancsmag egy **StorageAccountCredential** -objektumot ad eredményül, ha a *StorageAccountName* paramétert adja meg, vagy ha nem adja meg ezt a paramétert, akkor az a **IList \<StorageAccountCredential\>** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cfa47-125">This cmdlet returns a **StorageAccountCredential** object, if you specify the *StorageAccountName* parameter, or if you do not specify that parameter, it returns an **IList\<StorageAccountCredential\>** object.</span></span>

## <span data-ttu-id="cfa47-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfa47-126">NOTES</span></span>

## <span data-ttu-id="cfa47-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfa47-127">RELATED LINKS</span></span>

[<span data-ttu-id="cfa47-128">Új – AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cfa47-128">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="cfa47-129">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cfa47-129">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="cfa47-130">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cfa47-130">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)


