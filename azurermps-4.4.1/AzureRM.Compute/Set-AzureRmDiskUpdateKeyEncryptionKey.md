---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 2eadad8ff5a8f2c2036a6100a4af90eac1bff35a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492522"
---
# <span data-ttu-id="3ba8a-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3ba8a-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="3ba8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ba8a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba8a-103">A kulcs titkosítási kulcs tulajdonságait állítja be a lemez Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-103">Sets the key encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ba8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ba8a-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ba8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ba8a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba8a-106">A **set-AzureRmDiskUpdateKeyEncryptionKey** parancsmag a kulcs titkosítási kulcs tulajdonságát a Disk Update objektumban állítja be.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-106">The **Set-AzureRmDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="3ba8a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ba8a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ba8a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ba8a-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="3ba8a-109">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3ba8a-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3ba8a-111">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="3ba8a-112">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3ba8a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ba8a-113">PARAMETERS</span></span>

### <span data-ttu-id="3ba8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba8a-114">-DefaultProfile</span></span>
<span data-ttu-id="3ba8a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ba8a-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="3ba8a-116">-DiskUpdate</span></span>
<span data-ttu-id="3ba8a-117">Helyi merevlemez-frissítő objektum megadása</span><span class="sxs-lookup"><span data-stu-id="3ba8a-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba8a-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="3ba8a-118">-KeyUrl</span></span>
<span data-ttu-id="3ba8a-119">Specifes a legfontosabb URL-címet.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-119">Specifes the key Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba8a-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3ba8a-120">-SourceVaultId</span></span>
<span data-ttu-id="3ba8a-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="3ba8a-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ba8a-122">-Confirm</span></span>
<span data-ttu-id="3ba8a-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba8a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ba8a-124">-WhatIf</span></span>
<span data-ttu-id="3ba8a-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ba8a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ba8a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba8a-127">CommonParameters</span></span>
<span data-ttu-id="3ba8a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ba8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba8a-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba8a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba8a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ba8a-130">INPUTS</span></span>

### <span data-ttu-id="3ba8a-131">Microsoft. Azure. Management. kiszámítás. models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="3ba8a-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="3ba8a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba8a-132">System.String</span></span>

## <span data-ttu-id="3ba8a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ba8a-133">OUTPUTS</span></span>

### <span data-ttu-id="3ba8a-134">Microsoft. Azure. Management. kiszámítás. models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="3ba8a-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="3ba8a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ba8a-135">NOTES</span></span>

## <span data-ttu-id="3ba8a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ba8a-136">RELATED LINKS</span></span>

