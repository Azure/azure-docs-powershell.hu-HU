---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016259"
---
# <span data-ttu-id="0b69c-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="0b69c-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="0b69c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b69c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b69c-103">Importál egy konfigurációs fájlt.</span><span class="sxs-lookup"><span data-stu-id="0b69c-103">Imports a configuration file.</span></span>

## <span data-ttu-id="0b69c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b69c-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0b69c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b69c-105">DESCRIPTION</span></span>
<span data-ttu-id="0b69c-106">Az **import-AzureStorSimpleLegacyApplianceConfig** parancsmag importálja a konfigurációs fájlt a régi készülékről.</span><span class="sxs-lookup"><span data-stu-id="0b69c-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="0b69c-107">A fájl a mennyiségi tárolókkal, a biztonsági irányelvekkel és az Azure StorSimple szolgáltatáshoz tartozó tárolási fiók hitelesítő adataival kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0b69c-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="0b69c-108">Ez a parancsmag a régi készülék konfigurációs metaadatait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0b69c-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="0b69c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0b69c-109">EXAMPLES</span></span>

### <span data-ttu-id="0b69c-110">1. példa: konfigurációs fájl importálása</span><span class="sxs-lookup"><span data-stu-id="0b69c-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="0b69c-111">Ezzel a paranccsal importálhatja a konfigurációs fájlt a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="0b69c-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="0b69c-112">A parancs a fájl visszafejtéséhez a kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0b69c-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="0b69c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b69c-113">PARAMETERS</span></span>

### <span data-ttu-id="0b69c-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="0b69c-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="0b69c-115">A régi készülék konfigurációjának visszafejtési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b69c-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b69c-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="0b69c-116">-ConfigFilePath</span></span>
<span data-ttu-id="0b69c-117">A beolvasott konfigurációs fájl abszolút elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b69c-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b69c-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="0b69c-118">-Profile</span></span>
<span data-ttu-id="0b69c-119">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="0b69c-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0b69c-120">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="0b69c-120">-TargetDeviceName</span></span>
<span data-ttu-id="0b69c-121">A megcélzott eszköz nevét adja meg a portálon bemutatott módon.</span><span class="sxs-lookup"><span data-stu-id="0b69c-121">Specifies the name of the target device as presented in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b69c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b69c-122">CommonParameters</span></span>
<span data-ttu-id="0b69c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b69c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b69c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b69c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b69c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b69c-125">INPUTS</span></span>

### <span data-ttu-id="0b69c-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="0b69c-126">None</span></span>

## <span data-ttu-id="0b69c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b69c-127">OUTPUTS</span></span>

### <span data-ttu-id="0b69c-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b69c-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="0b69c-129">Ez a parancsmag a konfiguráció részleteit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0b69c-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="0b69c-130">A **LegacyApplianceConfiguration** objektum a következő információkat tartalmazza: konfigurációs azonosító, mennyiségi tárolók, hozzáférés-szabályozási rekordok, biztonsági házirendek, sávszélesség-beállítások, mennyiségi tárolók, a tárolási fiók hitelesítő adatai és a kötetek.</span><span class="sxs-lookup"><span data-stu-id="0b69c-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="0b69c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b69c-131">NOTES</span></span>

## <span data-ttu-id="0b69c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b69c-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b69c-133">Importálás – AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="0b69c-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


