---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: fa77808eddc0e51fa76a0883980b34552589f4ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850141"
---
# <span data-ttu-id="b4301-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b4301-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="b4301-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4301-102">SYNOPSIS</span></span>
<span data-ttu-id="b4301-103">Pillanatfelvételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b4301-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4301-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4301-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4301-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4301-105">DESCRIPTION</span></span>
<span data-ttu-id="b4301-106">A **New-AzureRmSnapshot** parancsmag pillanatképet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b4301-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="b4301-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b4301-107">EXAMPLES</span></span>

### <span data-ttu-id="b4301-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4301-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="b4301-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="b4301-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="b4301-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="b4301-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b4301-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b4301-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="b4301-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="b4301-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b4301-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4301-113">PARAMETERS</span></span>

### <span data-ttu-id="b4301-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4301-114">-AsJob</span></span>
<span data-ttu-id="b4301-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="b4301-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4301-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4301-116">-DefaultProfile</span></span>
<span data-ttu-id="b4301-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4301-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4301-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4301-118">-ResourceGroupName</span></span>
<span data-ttu-id="b4301-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4301-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b4301-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="b4301-120">-Snapshot</span></span>
<span data-ttu-id="b4301-121">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b4301-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4301-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b4301-122">-SnapshotName</span></span>
<span data-ttu-id="b4301-123">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4301-123">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4301-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4301-124">-Confirm</span></span>
<span data-ttu-id="b4301-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4301-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4301-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4301-126">-WhatIf</span></span>
<span data-ttu-id="b4301-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4301-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4301-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4301-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4301-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4301-129">CommonParameters</span></span>
<span data-ttu-id="b4301-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4301-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4301-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4301-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4301-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4301-132">INPUTS</span></span>

### <span data-ttu-id="b4301-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b4301-133">System.String</span></span>
<span data-ttu-id="b4301-134">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b4301-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b4301-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4301-135">OUTPUTS</span></span>

### <span data-ttu-id="b4301-136">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b4301-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="b4301-137">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b4301-137">System.Object</span></span>

## <span data-ttu-id="b4301-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4301-138">NOTES</span></span>

## <span data-ttu-id="b4301-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4301-139">RELATED LINKS</span></span>

