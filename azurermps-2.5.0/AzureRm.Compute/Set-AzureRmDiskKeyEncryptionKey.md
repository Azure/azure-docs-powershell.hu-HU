---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskkeyencryptionkey
schema: 2.0.0
ms.openlocfilehash: 1a3cbf9037f81d9387b1979472e50be940caa7d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849713"
---
# <span data-ttu-id="04510-101">Set-AzureRmDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="04510-101">Set-AzureRmDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="04510-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04510-102">SYNOPSIS</span></span>
<span data-ttu-id="04510-103">A kulcs titkosítási kulcs tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="04510-103">Sets the key encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04510-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04510-104">SYNTAX</span></span>

```
Set-AzureRmDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04510-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04510-105">DESCRIPTION</span></span>
<span data-ttu-id="04510-106">A **set-AzureRmDiskKeyEncryptionKey** parancsmag a fontos titkosítási kulcs tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="04510-106">The **Set-AzureRmDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="04510-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04510-107">EXAMPLES</span></span>

### <span data-ttu-id="04510-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="04510-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="04510-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="04510-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="04510-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="04510-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="04510-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="04510-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="04510-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="04510-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="04510-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04510-113">PARAMETERS</span></span>

### <span data-ttu-id="04510-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04510-114">-DefaultProfile</span></span>
<span data-ttu-id="04510-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04510-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04510-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="04510-116">-Disk</span></span>
<span data-ttu-id="04510-117">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="04510-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04510-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="04510-118">-KeyUrl</span></span>
<span data-ttu-id="04510-119">Specifes a legfontosabb URL-címet.</span><span class="sxs-lookup"><span data-stu-id="04510-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="04510-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="04510-120">-SourceVaultId</span></span>
<span data-ttu-id="04510-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="04510-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="04510-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04510-122">-Confirm</span></span>
<span data-ttu-id="04510-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04510-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04510-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04510-124">-WhatIf</span></span>
<span data-ttu-id="04510-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04510-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04510-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04510-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04510-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04510-127">CommonParameters</span></span>
<span data-ttu-id="04510-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04510-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04510-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04510-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04510-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04510-130">INPUTS</span></span>

### <span data-ttu-id="04510-131">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="04510-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="04510-132">System. String</span><span class="sxs-lookup"><span data-stu-id="04510-132">System.String</span></span>

## <span data-ttu-id="04510-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04510-133">OUTPUTS</span></span>

### <span data-ttu-id="04510-134">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="04510-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="04510-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04510-135">NOTES</span></span>

## <span data-ttu-id="04510-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04510-136">RELATED LINKS</span></span>

